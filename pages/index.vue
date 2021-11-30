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
    <div class="advantages">
      <Advantage
        v-for="(advantage, itemObjKey) in advantages"
        :key="itemObjKey + 1"
        :advantage="advantage"
      />
    </div>
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
        <Button
          class="product-responsibility__btn"
          type="button"
          text="Obtenir un devis"
        />
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
    <div class="our-range">
      <h1 class="our-range__title">Notre gamme</h1>
      <div class="our-range__cards">
        <Card
          v-for="(product, itemObjKey) in products"
          :key="itemObjKey + 1"
          :product="product"
        />
      </div>
    </div>
    <div class="natural-mattress">
      <h1 class="natural-mattress__title">Le matelas en latex naturel</h1>
      <div class="natural-mattress__img"></div>
      <div class="natural-mattress__bloc-text">
        <div class="natural-mattress__bloc-text-left">
          <p>
            Pour des nuits confortables mais avant tonaturelles, le matelas
            latex naturel Kipli est votre meilleur allié. Pour des nuits
            confortables mais avant tout naturelles, le matelas latex naturel
            kipli est votre meilleur allié. Pour des nuits confortables mais
            avant tout naturelles, le matelas latex naturel Kipli est votre
            meilleur allié. Pour des nuits confortables mais avant tout
          </p>
        </div>
        <div class="natural-mattress__bloc-text-right">
          <p>
            Pour des nuits confortables mais avant tonaturelles, le matelas
            latex naturel Kipli est votre meilleur allié. Pour des nuits
            confortables mais avant tout naturelles, le matelas latex naturel
            kipli est votre meilleur allié. Pour des nuits confortables mais
            avant tout naturelles, le matelas latex naturel Kipli est votre
            meilleur allié. Pour des nuits confortables mais avant tout
          </p>
        </div>
        <img
          class="natural-mattress__icon"
          src="../assets/images/picto_scroll.svg"
          alt="scroll"
        />
      </div>
      <div class="natural-mattress__slogan">
        <img src="../assets/images/slogan.png" alt="slogan" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    advantages: [
      {
        title: 'Résilience et maintien',
        img: require('../assets/images/advantage1.svg'),
        desc: "Nos matelas s'adaptent au dormeur et non l'inverse",
      },
      {
        title: 'Matières naturelles',
        img: require('../assets/images/advantage2.svg'),
        desc: 'Nos matelas sont extrêments respirants, déhoussables, anti acariens et antibactériens',
      },
      {
        title: 'Economiques et écologique',
        img: require('../assets/images/advantage3.svg'),
        desc: 'Des coûts optimisés grâce à une durée de vie double',
      },
      {
        title: 'Prix réduits',
        img: require('../assets/images/advantage4.svg'),
        desc: 'Des tarifs professionnels avantageux',
      },
      {
        title: 'Un chargé de compte dédié',
        img: require('../assets/images/advantage5.svg'),
        desc: 'Un accompagnement marketing sur-mesure',
      },
    ],
    products: [
      {
        img: require('../assets/images/bedframe1.jpeg'),
        title: 'Commode Picardie',
        specificities: ['Bois de hêtre massif', 'Lattes flexibles ou rigides'],
        price: '700€',
      },
      {
        img: require('../assets/images/bedframe2.jpeg'),
        title: 'Table de chevet Picardie',
        specificities: ['Epicéa massif', 'Lattes rigides'],
        price: '700€',
      },
      {
        img: require('../assets/images/bedframe3.jpeg'),
        title: 'Etagère Picardie',
        specificities: ['Bois de hêtre massif', 'Lattes flexibles ou rigides'],
        price: '700€',
      },
    ],
  }),
}
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

.advantages {
  display: flex;
  justify-content: space-between;
  justify-content: center;
  align-items: center;
  margin: 40px 0;
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
    width: 35%;
  }
}

.customers {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0 80px;
  margin: 40px 0;

  &__title {
    font-size: 1.4em;
    margin-bottom: 60px;
  }

  &__img {
    width: 90%;
  }
}

.our-range {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 40px 0;
  &__title {
    width: 90%;
    margin-left: 5%;
    font-size: 1.4em;
  }
  &__cards {
    display: flex;
    justify-content: space-around;
    align-content: center;
    width: 90%;
  }
}

.natural-mattress {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 40px 0;
  &__title {
    width: 90%;
    margin-left: 5%;
    font-size: 1.4em;
  }
  &__img {
    height: 300px;
    width: 100%;
    background-image: url('../assets/images/matelas_latex_naturel.png');
    background-position: center;
    background-size: cover;
    /* -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover; */
    background-repeat: no-repeat;
    margin-top: 40px;
  }
  &__bloc-text {
    position: relative;
    width: 80%;
    display: flex;
    justify-content: space-between;
    margin-top: 40px;
    div {
      position: relative;
      margin: 0 20px;
      &:after {
        position: absolute;
        bottom: 0;
        height: 100%;
        width: 100%;
        content: '';
        background: linear-gradient(
          to top,
          rgba(255, 255, 255, 1) 5%,
          rgba(255, 255, 255, 0) 80%
        );
        pointer-events: none;
      }
    }
    p {
      text-align: center;
      letter-spacing: 0.2px;
      line-height: 1.2em;
    }
  }
  &__icon {
    cursor: pointer;
    height: 40px;
    position: absolute;
    bottom: -15px;
    margin-left: auto;
    margin-right: auto;
    left: 0;
    right: 0;
    transform: rotate(86deg);
  }
  &__slogan {
    width: 50%;
    display: flex;
    justify-content: center;
    margin-top: 40px;
  }
}

@media only screen and (max-width: 450px) {
  .landing {
    flex-direction: column;
    justify-content: space-between;
    background-size: contain;
    background-repeat: initial;

    &__title {
      position: static;
      img {
        display: none;
      }
    }
  }

  .advantages {
    flex-direction: column;
    width: 100%;
  }

  .product-responsibility {
    &__leaf1 {
      height: 55px;
    }
    &__leaf2 {
      height: 130px;
    }

    &__wrapper {
      width: 80%;
    }

    &__title {
      text-align: center;
    }

    &__desc {
      margin-top: 55px;
    }

    &__btn {
      width: 100%;
    }
  }

  .customers {
    padding: 0;
  }

  .our-range {
    &__title {
      text-align: center;
      margin-left: 0;
    }
    &__cards {
      flex-direction: column;
    }
  }

  .natural-mattress {
    &__title {
      text-align: center;
      margin-left: 0;
    }

    &__img {
      height: 100px;
      background-size: contain;
      background-position: initial;
    }

    &__bloc-text {
      width: 95%;
      margin-top: 0;
    }

    &__slogan {
      width: 100%;

      img {
        width: 100%;
      }
    }
  }
}
</style>
