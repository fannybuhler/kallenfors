<template>
  <div class="intro" :class="`intro--${modifier}`">
    <div class="intro__column intro__column--image">
      <div class="intro__color"></div>
      <div class="intro__media">
        <img class="intro__image" v-if="image" :src="require(`@/assets/images/${image}`)" :alt="alt" />
        <div class="intro__overlay" v-if="firstName">
          <h3 class="intro__overlay-heading" v-html="firstName" />
          <h3 class="intro__overlay-heading" v-html="lastName" />
          <NuxtLink class="intro__overlay-link" :to="link" v-if="link">
            Mer om {{ firstName }} <i class="arrow right"></i>
          </NuxtLink>
        </div>
      </div>
    </div>
    <div class="intro__column">
      <div class="intro__info">
        <h3 class="intro__heading intro__heading--uc" v-html="heading" />
        <div v-if="span" class="intro__span"></div>
        <p class="intro__body">
          {{ description }}
          <a  class="intro__external-link" v-if="externalLink" :href="externalLink">här</a>
        </p>
        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    modifier: String,
    link: String,
    alt: String,
    firstName: String,
    lastName: String,
    image: String,
    heading: String,
    description: String,
    externalLink: String,
    span: {
      type: Boolean,
      default: true
    },
  }
}
</script>

<style lang="scss" scoped>
.intro {
  $b: &;
  @include pageWrap();
  @include mainContent();
  @include blockPadding();
  overflow: hidden;
  flex-direction: column;

  @media only screen and (min-width: $tablet) {
    display: flex;
    align-items: center;

    &--image-left {
      flex-direction: row;
    }

    &--image-right {
      flex-direction: row-reverse;
    }
  }

  &__column {
    flex: 1;
    position: relative;

    &--image {
      // width: 80%;
      max-width: 450px;
      
      #{$b}--image-left & {
        padding-right: 20%;
      }

      #{$b}--image-right & {
        padding-left: 20%;
      }

      @media only screen and (min-width: $tablet) {
        width: 100%;
        max-width: none;
        
        #{$b}--image-left & {
          padding-right: 0;
        }

        #{$b}--image-right & {
          padding-left: 0;
        }
      }
    }
  }

  &__color {
    z-index: 1;
    position: absolute;
    background: $pop;
    top: 35%;
    height: 30%;
    width: 100%;

    #{$b}--image-left & {
      left: -11.25%;
    }

    #{$b}--image-right & {
      right: -11.25%;
    }

    @media only screen and (min-width: $tablet) {
      width: 105%;
    }
  }

  &__media {
    z-index: 2;
    position: relative;
    margin-bottom: 1.5rem;

    @media only screen and (min-width: $tablet) {
      margin-bottom: 0;

      #{$b}--image-left & {
        margin-right: 20%;
      }

      #{$b}--image-right & {
        margin-left: 20%;
      }
    }
  }

  &__image {
    width: 100%;
    display: block;
  }

  &__overlay {
    color: #fff;
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    text-align: center;
    background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
    padding: 10px 0;
  }

  &__overlay-heading {
    @include h2();
    font-size: 32px;
    color: $pop;
    text-transform: none;
    margin: 5px 0;
  }

  &__overlay-link {
    color: inherit;
    text-decoration: none;
    padding: 10px;
  }

  &__info {
    line-height: 160%;
  }

  &__heading {
    @include h3();
    font-weight: 300;
    line-height: 160%;
    margin-bottom: 1.5rem;

    &--uc {
      text-transform: uppercase;
    }
  }

  &__span {
    background: black;
    height: 1px;
    width: 30%;
    // margin: 1.5rem 0;
    z-index: 2;
  }

  &__body {
    margin-top: 1.5rem;
  }

  &__external-link {
    text-decoration-color: $pop;
    color: black;
    font-size: 1.4rem;
    vertical-align: text-top;
    text-transform: uppercase;

    &:hover {
      text-decoration-color: $darkpop;
    }
  }
}
</style>
