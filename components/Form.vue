<template>
  <form class="form" @submit.prevent="submitForm">
    <img class="form__logo" src="../assets/images/kipli_logo.svg" />
    <div class="form__bg">
      <div class="form__content">
        <div class="form__desc">
          <p>Obtenir un devis gratuit</p>
          <p>
            Equipez votre établissement avec une literie saine, confortable et
            au prix juste :
          </p>
        </div>
        <div class="form__identity">
          <div class="flex">
            <label class="required"></label>
            <input
              v-model="name"
              required="required"
              type="text"
              placeholder="Prénom"
            />
          </div>
          <div class="flex">
            <label class="required"></label>
            <input
              v-model="lastname"
              required="required"
              type="text"
              placeholder="Nom"
            />
          </div>
        </div>
        <div class="flex">
          <label class="required"></label>
          <input
            v-model="email"
            required="required"
            type="email"
            placeholder="Email"
          />
        </div>
        <div class="flex">
          <label class="required"></label>
          <input
            v-model="tel"
            required="required"
            type="tel"
            placeholder="Téléphone"
          />
        </div>
        <div class="flex">
          <label class="required"></label>
          <input
            required="required"
            type="text"
            placeholder="Site internet ou Entreprise"
          />
        </div>
        <div class="flex">
          <label class="required hidden"></label>
          <textarea v-model="message" type="text" placeholder="Votre message" />
        </div>
        <div class="flex">
          <label class="required hidden"></label>
          <Button class="form__btn" type="submit" text="Envoyer ma demande" />
        </div>
        <p class="form__info">Nous vous répondrons sous 48h</p>
      </div>
    </div>
  </form>
</template>

<script>
import useValidate from '@vuelidate/core'
import { required, email, minLength } from '@vuelidate/validators'
export default {
  data() {
    return {
      v$: useValidate(),
      name: '',
      lastname: '',
      email: '',
      tel: '',
      message: '',
      submitted: false,
    }
  },
  validations() {
    return {
      name: { required, minLength: minLength(3) },
      lastname: { required, minLength: minLength(3) },
      email: { required, email },
      tel: { required },
      message: {},
    }
  },
  methods: {
    submitForm() {
      // console.log(this.v$)
      this.submitted = true
    },
  },
}
</script>

<style lang="scss" scoped>
.flex {
  display: flex;
}

.form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 34%;
  margin-left: 6%;

  &__logo {
    height: 25px;
    width: 50%;
    padding: 20px;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  &__bg {
    background-color: #f0f6ed;
    display: flex;
    justify-content: center;
  }

  &__content {
    display: flex;
    flex-direction: column;
    width: 80%;
    padding: 10px;

    .form__desc {
      display: flex;
      flex-direction: column;
      align-items: center;
      p:nth-of-type(1) {
        font-size: 1.2em;
        font-weight: bold;
        margin-bottom: 10px;
      }
      p:nth-of-type(2) {
        margin-top: 0;
        font-size: 1em;
        text-align: center;
      }
    }

    .form__identity {
      width: 100%;
      display: flex;
      justify-content: space-between;
      input {
        width: 100%;
      }
    }

    label {
      margin-right: 6px;
      margin-left: 6px;
    }

    textarea {
      font-family: inherit;
      font-size: inherit;
      resize: none;
      height: 80px !important;
      width: 0;
    }

    input,
    textarea {
      font-size: 1em;
      height: 30px;
      width: 100%;
      margin: 6px 0;
      padding: 4px 0;
      border: 1px solid #bed4cd;
      text-indent: 10px;

      &::placeholder {
        color: #c4c4c4;
      }

      &:focus {
        color: #305157;
        outline: 1px solid #305157;
        border: none;
      }
    }

    .required:after {
      content: ' *';
      color: red;
      font-size: 0.8em;
    }

    .hidden:after {
      visibility: hidden;
    }

    .form__btn {
      width: 100%;
    }

    .form__info {
      text-align: center;
      font-size: 0.9em;
      color: #41c7c0;
    }
  }
}

@media only screen and (max-width: 450px) {
  .form {
    width: 100%;
    margin-left: 0;
    margin-top: 20px;
  }
}
</style>
