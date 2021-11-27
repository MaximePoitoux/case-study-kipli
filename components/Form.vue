<template>
  <div class="wrapper-form">
    <div>
      <img class="logo" src="../assets/images/kipli_logo.svg" />
      <div class="form">
        <div class="form__content">
          <div class="form__desc">
            <p>Obtenir un devis gratuit</p>
            <p>
              Equipez votre établissement avec une literie saine, confortable et
              au prix juste :
            </p>
          </div>
          <div class="form__identity">
            <input type="text" placeholder="Prénom" />
            <input type="text" placeholder="Nom" />
          </div>
          <input type="email" placeholder="Email" />
          <input type="tel" placeholder="Téléphone" />
          <input type="text" placeholder="Site internet ou Entreprise" />
          <textarea type="text" placeholder="Votre message" />
          <button type="submit">Envoyer ma demande</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.wrapper-form {
  height: auto;
  width: 30%;
}

.logo {
  height: 25px;
}

.form {
  background-color: #f0f6ed;
  display: flex;
  flex-direction: column;
  align-items: center;

  &__content {
    width: 90%;
    input,
    textarea {
      font-size: 1em;
      height: 30px;
      width: 100%;
      margin: 8px 0;
      padding: 5px 0 5px 8px;
      border: 1px solid #d8e5dd;

      &::placeholder {
        color: #c4c4c4;
      }

      &:focus {
        color: #305157;
        outline: 1px solid #305157;
        border: none;
      }
    }

    .form__desc {
      display: flex;
      flex-direction: column;
      align-items: center;
      p:nth-of-type(1) {
        font-size: 1.2em;
        font-weight: bold;
      }
      p:nth-of-type(2) {
        font-size: 1em;
        text-align: center;
      }
    }
  }

  &__identity {
    display: flex;
    align-items: center;
    /* input {
      font-size: 1em;
      height: 30px;
      margin: 8px 0;
      padding: 5px 0 5px 8px;
      border: 1px solid#d8e5dd;
    }
    input:nth-of-type(1) {
      margin-right: 10%;
    } */
  }
}
</style>
