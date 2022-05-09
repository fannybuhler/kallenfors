<template>
  <div class="footer">
    <div class="footer__wrapper">
      <div class="footer__form-wrapper">
        <h3 class="footer__heading">Maila oss</h3>
        <form class="footer__form" @submit.prevent="submitForm">
          <input
            type="checkbox"
            name="botcheck"
            id=""
            style="display: none"
          />
          <p>
            <label for="name">
              NAMN <br>
              <input type="text" name="name" id="name" required v-model="form.name">
            </label>
          </p>
          <p>
            <label for="email">
              E-POST<br>
              <input type="text" name="email" id="email" required v-model="form.email">
            </label>
          </p>
          <p>
            <label for="message">
              MEDDELANDE<br>
              <textarea name="message" placeholder="Skriv ditt meddelande här..." id="message" required v-model="form.message"></textarea>
            </label>
          </p>
          <button class="footer__send-form-button" type="submit">Skicka</button>
          <p v-if="result">{{ result }}</p>
        </form>
      </div>
      <div class="footer__info-wrapper">
        <h4 class="footer__subheading">Kontakt</h4>
        <p class="footer__info-heading">Mail</p>
        <a class="footer__info-body" href="mailto:anna-karin@kallenfors.com">anna-karin@kallenfors.com</a>
        <a class="footer__info-body footer__info-body--last" href="mailto:peter@kallenfors.com">peter@kallenfors.com</a>
        <p class="footer__info-heading">Telefon</p>
        <a class="footer__info-body footer__info-body--last" href="tel:0702678303">070-267 83 03</a>
        <p class="footer__info-heading">Adress Stockholm</p>
        <p class="footer__info-body footer__info-body--last">Bragevägen 21, <br> 114 24 Stockholm</p>
        <p class="footer__info-heading">Adress Sundsvall</p>
        <p class="footer__info-body footer__info-body--last">Skärsätt 118, <br> 862 95 Njurunda</p>
        <h4 class="footer__subheading">Information</h4>
        <p class="footer__info-heading">Fakturainfo</p>
        <p class="footer__info-body">inbox.lev851158@arkivplats.se</p>
        <p class="footer__info-body footer__info-body--last">559175-1440</p>
        <p class="footer__copyright">© 2021 KÄLLENFORS</p>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      form: {
        apikey: "58e602b2-5bf5-4fcc-9515-139aa10f755a",
        subject: "Nytt mail från Kallenfors.com",

        name: "",
        email: "",
        message: "",
      },
      result: "",
      status: "",
    };
  },
  methods: {
    async submitForm(e) {
      this.result = "Skickar...";
      axios.create({
        headers: { "Content-Type": "application/json" },
      });
      await axios
        .post("https://api.web3forms.com/submit", this.form)
        .then(async (response) => {
          //let json = await response.json();
          //this.result = json.message;
          console.log(response);
          this.result = response.data.message;

          if (response.status === 200) {
            this.status = "success";
          } else {
            console.log(response);
            this.status = "error";
          }
        })
        .catch((error) => {
          console.log(error);
          this.status = "error";
          this.result = "Något gick fel!";
        })
        .then(() => {
          const form = this.form;
          form.name = "";
          form.email = "";
          form.message = "";

          setTimeout(() => {
            this.result = "";
            this.status = "";
          }, 5000);
        });
    },
  },
};
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
  margin-bottom: 15px;
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

a {
  text-decoration: none;
  color: #fff;
  display: block;
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
  margin: 0 auto;
  padding: 3rem 5%;
  padding-bottom: calc(3rem + 25px);

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
    height: 50px;
    line-height: 130%;
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
    height: 50px;
    line-height: 173%;
  }

  &__info-heading {
    text-transform: uppercase;
    font-size: 20px;
    margin: 0;
    line-height: 160%;
  }

  &__info-body {
    font-size: 16px;
    margin: 0;
    line-height: 160%;

    &--last {
      padding-bottom: 30px;
    }
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
    cursor: pointer;
    transition: 0.1s;

    &:hover {
      background: $darkpop;
    }
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