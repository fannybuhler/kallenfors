<template>
  <div class="intro">
    <div class="intro__media">
      <div class="intro__color-block"></div>
      <div class="intro__image-wrapper">
        <img class="intro__image" src="@/assets/images/photos/peter.jpeg" alt="Porträttfoto av Peter Källenfors avslappnat klädd">
        <div class="intro__image-overlay">
          <h3 class="intro__image-overlay__heading">Peter<br>Källenfors</h3>
          <NuxtLink to="/peter-kallenfors">
            Läs mer om Peters arbete <i class="arrow right"></i>
          </NuxtLink>
        </div>
      </div>
    </div>
    <div class="intro__content">
      <h3 class="intro__heading">25 års erfarenhet av att leverera juridik på en hög kvalitativ nivå.</h3>
      <div class="intro__span"></div>
      <p class="intro__body">Peter Källenfors har mångårig erfarenhet av att lämna rådgivning vid x, y och z samt i bolagsrättsliga frågor. Peter arbetar även regelbundet med alla typer av kommersiella tvister och i skiljeförfaranden.
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
a {
  text-decoration: none;
}

.intro {
  // @include boxer(red);
  // padding: 0 5%;

  @media only screen and (min-width: $tablet) {
    display: flex;
    align-items: center;
  }

  &__media {
    flex: 1;
    position: relative;
  }

  &__image-wrapper {
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

  &__image-overlay {
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    text-align: center;
    background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
  }

  &__color-block {
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

  /*
  margin: 3rem 0;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;

  &__image-wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    position: relative;
  }

  &__color-block {
    width: 85%;
    background-color: #F8BD59;
    z-index: -1;
    grid-column: 1 / 4;
    grid-row: 2 / 3;
  }

  &__image {
    height: auto;
    width: 70%;
    margin-left: -12%;
    z-index: 1;
    max-height: 724px;
    max-width: 550px;
    grid-column: 1 / 4;
    justify-self: center;
    align-self: center;
    grid-row: 1 / 4;
  }

  &__image-overlay {
    background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
    grid-column: 1 / 4;
    grid-row: 1 / 4;
    justify-self: center;
    align-self: center;
    height: 40%;
    width: 70%;
    max-height: 724px;
    max-width: 550px;
    position: absolute;
    bottom: 0;
    margin-left: -12%;
    z-index: 2;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;

    &__heading {
      color: $pop;
      font-family: 'Playfair regular';
      line-height: 130%;
      font-size: 24px;
      text-align: center;
      margin: 0;
    }

    &__body {
      color: #fff;
      font-size: 12px;
    }
  }
  */

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
  }

  &__body {
    margin: 0 20px;
  }

  /*
  @media only screen and (min-width: $tablet) {
    .intro {
      &__image-wrapper {
        width: 50%;

      }

      &__image-overlay {
        &__heading {
          font-size: 42px;
        }

        &__body {
          font-size: 18px;
        }
      }

      &__content-wrapper {
        width: 50%;
        align-self: center;
      }

      &__color-block {
        width: 100%;
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
      &__image-overlay {
        &__heading {
          font-size: 46px;
        }
      }
    }
  }
  */
}

</style>
