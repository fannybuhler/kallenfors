<template>
  <div class="footer">
    <div class="footer__wrapper">
      <div class="footer__form-wrapper">
        <h3 class="footer__heading">Maila oss</h3>
        <form class="footer__form" action="">
          <input type="hidden">
          <p>
            <label>
              NAMN <br>
              <input type="text" name="name">
            </label>
          </p>
          <p>
            <label>
              E-POST<br>
              <input type="text" name="email">
            </label>
          </p>
          <p>
            <label>
              MEDDELANDE<br>
              <textarea name="body" placeholder="Skriv ditt meddelande här..."></textarea>
            </label>
          </p>
          <p>
            <input class="footer__send-form-button" type="submit" value="Skicka">
          </p>
        </form>
      </div>
      <div class="footer__info-wrapper">
        <h4 class="footer__subheading">Kontakt</h4>
        <p class="footer__info-heading">Mail</p>
        <p class="footer__info-body">info@kallenfors.com</p>
        <p class="footer__info-heading">Telefon</p>
        <p class="footer__info-body">070-267 83 03</p>
        <p class="footer__info-heading">Adress Stockholm</p>
        <p class="footer__info-body">Bragevägen 21, <br> 112 24 Stockholm</p>
        <p class="footer__info-heading">Adress Sundsvall</p>
        <p class="footer__info-body">Skärsätt 118, <br> 862 95 Njurunda</p>
        <h4 class="footer__subheading">Information</h4>
        <p class="footer__info-heading">Fakturainfo</p>
        <p class="footer__copyright">© 2021 KÄLLENFORS</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
input, 
textarea {
  outline: 0;
  border-width: 0 0 2px;
  border-color: #fff;
  background: transparent;
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  transition: border-color .3s ease-in-out;
  width: 99%;
  padding-top: 10px;
}

textarea {
  height: 5rem;
}

label {
  font-family: Montserrat;
  font-size: 20px;
}

input:hover,
textarea:hover {
  border-color: $pop;
}

input:-webkit-autofill,
input:-webkit-autofill:hover, 
input:-webkit-autofill:focus,
textarea:-webkit-autofill,
textarea:-webkit-autofill:hover,
textarea:-webkit-autofill:focus,
select:-webkit-autofill,
select:-webkit-autofill:hover,
select:-webkit-autofill:focus
{
 box-shadow: 0 0 0 30px $black inset;
 -webkit-box-shadow: 0 0 0 30px $black inset;
 -webkit-text-fill-color: white !important;
}

.footer {
  background: $black;
  color: #fff;
  padding: 20px;
  margin: 0 auto;

  &__wrapper {
    max-width: 1200px;
    display: flex;
    flex-direction: column;
    margin: 0 auto;
  }

  &__heading {
    text-transform: uppercase;
    font-family: 'Playfair regular';
    font-size: 3rem;
    margin: 25px 0 15px 0;
  }

  &__form {
    width: 100%;
  }

  &__subheading {
    text-transform: uppercase;
    font-family: 'Playfair regular';
    font-size: 2.5rem;
    font-weight: 300;
    margin: 25px 0 15px 0;
  }

  &__info-heading {
    text-transform: uppercase;
    font-size: 20px;
    margin: 0;
  }

  &__info-body {
    font-size: 16px;
    margin: 0;
    padding-bottom: 30px;
  }

  &__send-form-button {
    background: $pop;
    border: none;
    width: fit-content;
    padding: 10px 15px;
    text-transform: uppercase;
    font-weight: 400;
    letter-spacing: 4px;
    float: right;
    color: #000;
  }

  &__copyright {
    font-size: 12px;
    margin: 0;
  }

  @media only screen and (min-width: $tablet) {
    
    .footer {
      &__wrapper {
        flex-direction: row-reverse;
      }

      &__form-wrapper {
        width: 50%;
      }

      &__info-wrapper {
        width: 50%;
      }
    }
  }
}
</style>