<template>
  <div class="intro-right">
    <div class="intro-right__image-wrapper">
      <div class="intro-right__color-block"></div>
      <img class="intro-right__image" src="@/assets/images/photos/anna-karin.jpeg" alt="Porträttfoto av Anna-Karin Källenfors avslappnat klädd">
      <div class="intro-right__image-overlay">
        <h3 class="intro-right__image-overlay__heading">Anna-Karin<br>Källenfors</h3>
        <NuxtLink to="/anna-karin-kallenfors">
         <p class="intro-right__image-overlay__body">Läs mer om Anna-Karins arbete <i class="arrow right"></i></p>
        </NuxtLink>
      </div>
    </div>
    <div class="intro-right__content-wrapper">
      <h3 class="intro-right__heading">I dagens brus krävs en grundlig och noggrann planering för marknadsföringen.</h3>
      <div class="intro-right__span"></div>
      <p class="intro-right__body">Anna-Karin Källenfors har 15 års erfarenhet av att projektledning, 
        kampanjutveckling och digitala kommunikationsstrategier. 
        Anna-Karin arbetar även regelbundet med löpande marknadsstöd och uppföljning.
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
a {
  text-decoration: none;
}

.intro-right {
  margin: 3rem 0;
  display: flex;
  flex-direction: row-reverse;
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
    justify-self: end;
  }

  &__image {
    height: auto;
    width: 70%;
    margin-right: -12%;
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
    margin-right: -12%;
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

  @media only screen and (min-width: $tablet) {
    .intro-right {
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
        margin-right: -15%;
      }
      
      &__body {
        font-size: 22px;
      }
    }
  }

  @media only screen and (min-width: $desktop) {
    .intro-right {
      &__image-overlay {
        &__heading {
          font-size: 46px;
        }
      }
    }
  }
}
</style>