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
        <div class="intro__span"></div>
        <p class="intro__body" v-html="description" />
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
    description: String
  }
}
</script>

<style lang="scss" scoped>
.intro {
  $b: &;
  @include mainContent();
  padding-bottom: 3rem;
  overflow: hidden;

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

    &--uc {
      text-transform: uppercase;
    }
  }

  &__span {
    background: black;
    height: 1px;
    width: 30%;
    margin: 1.5rem 0;
    z-index: 2;
  }

  &__body {
    //
  }


  /*
  @media only screen and (min-width: $tablet) {
    display: flex;
    align-items: center;
  }

  &__media {
    flex: 1;
    position: relative;
  }

  &__media {
    z-index: 2;
    position: relative;
    display: block;
    width: 75%;
    margin-left: 10%;
  }

  &__image {
    display: block;
    width: 100%;
  }

  &__overlay {
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    text-align: center;
    background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
    padding: 10px 0;

     &__heading {
      color: $pop;
      font-family: 'Playfair regular';
      line-height: 130%;
      font-size: 24px;
      text-align: center;
    }

    &__body {
      color: #fff;
      font-size: 12px;
    }
  }

  &__color {
    z-index: 1;
    position: absolute;
    left: 0;
    top: 50% - (40% * 0.5);
    width: 95%;
    height: 40%;
    background: $pop;

    @media only screen and (min-width: $tablet) {
      width: 100%;
    }
  }

  &__content {
    flex: 1;
  }

  &__heading {
    font-size: 26px;
    margin: 20px 20px;
    text-transform: uppercase;
  }

  &__span {
    background: black;
    height: 1px;
    width: 30%;
    margin: 20px 20px;
    z-index: 2;
  }

  &__body {
    margin: 0 20px;
  }


  @media only screen and (min-width: $tablet) {
    .intro {
      &__overlay {
        &__heading {
          font-size: 42px;
        }

        &__body {
          font-size: 18px;
        }
      }

      &__heading {
        font-size: 33px;
      }

      &__span {
        margin-left: -15%;
      }

      &__body {
        font-size: 22px;
      }
    }
  }

  @media only screen and (min-width: $desktop) {
    .intro {
      &__overlay {
        &__heading {
          font-size: 46px;
        }
      }
    }
  }
  */
}
</style>
