<template>
  <div>
    <RatingBar />
    <div class="landing">
      <div class="landing__title">
        <p>Pour les professionnels <br />et l'hôtellerie</p>
        <img src="../assets/images/arrow.svg" alt="arrow" />
      </div>
      <Form />
    </div>
    <Advantages />
    <div class="product-responsibility">
      <img
        src="../assets/images/leaf1.svg"
        alt="leaf"
        class="product-responsibility__leaf1"
      />
      <div class="product-responsibility__wrapper">
        <h1 class="product-responsibility__title">Des produits responsables</h1>
        <p class="product-responsibility__desc">
          Aujourd'hui, 70% des voyageurs sont plus susceptibles de réserver un
          hébergement ayant pris des mesures éco-responsables. Proposez une
          alternative saine et durable à vos hôtes en adoptant la literie Kipli
          !
        </p>
        <button class="product-responsibility__btn">Obtenir un devis</button>
      </div>
      <img
        src="../assets/images/leaf2.svg"
        alt="leaf"
        class="product-responsibility__leaf2"
      />
    </div>
    <div class="customers">
      <h1 class="customers__title">Ils nous font confiance</h1>
      <img
        src="../assets/images/customers.png"
        alt="They trust us"
        class="customers__img"
      />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
@font-face {
  font-family: 'Mackinac';
  font-style: normal;
  font-weight: 400;
  font-display: swap;
  src: url('../assets/fonts/P22Mackinac-Book_13.otf') format('otf');
}

body {
  margin: 0;
  font-family: Mackinac, ui-sans-serif, system-ui;
  color: #305157;
}

.landing {
  position: relative;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  height: 700px;
  background-image: url(../assets/images/matelas-home.jpeg);
  background-attachment: fixed;
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;

  &__title {
    position: absolute;
    top: 2%;
    right: 24%;
    font-size: 1.8em;
    p {
      text-align: center;
      margin-bottom: 0;
    }

    img {
      height: 50px;
      transform: rotate(-35deg);
      margin-left: 18px;
    }
  }
}

.product-responsibility {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 40px 0;

  &__leaf1 {
    height: 100px;
    position: absolute;
    top: 0;
    left: 0;
  }

  &__leaf2 {
    height: 240px;
    position: absolute;
    top: 0;
    right: 0;
  }

  &__wrapper {
    width: 50%;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-image: url(../assets/images/galet.svg);
    background-size: 70%;
    background-position: center 80px;
    background-repeat: no-repeat;
    padding: 40px 0;
  }

  &__title {
    font-size: 1.8em;
  }

  &__desc {
    text-align: center;
    line-height: 1.5em;
    letter-spacing: 0.8px;
  }

  &__btn {
    cursor: pointer;
    margin-top: 10px;
    padding: 10px;
    font-size: 1em;
    background-color: #b85e4c;
    color: white;
    border: none;
    margin-top: 20px;
    width: 35%;
  }
}

.customers {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0 80px;

  &__title {
    font-size: 1.4em;
    margin-bottom: 60px;
  }

  &__img {
    width: 90%;
  }
}
</style>
