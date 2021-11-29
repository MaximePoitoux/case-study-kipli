<template>
  <div class="card">
    <div class="card__img">
      <img :src="product.img" :alt="product.title" />
    </div>
    <div class="card__content">
      <div class="card__header">
        <p class="card__title">{{ product.title }}</p>
        <div class="card__icons-list">
          <img
            class="card__icon"
            src="../assets/images/picto_france.svg"
            alt="france"
          />
          <img
            class="card__icon"
            src="../assets/images/picto_pefc.svg"
            alt="pefc"
          />
        </div>
      </div>
      <ul
        v-for="(specificity, itemObjKey) in product.specificities"
        :key="itemObjKey + 1"
        class="card__specificities"
      >
        <li class="card__specificity">{{ specificity }}</li>
      </ul>
      <p class="card__price">
        <span class="card__price-small">À partir de</span> {{ product.price }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.card {
  cursor: pointer;
  display: flex;
  flex-direction: column;
  width: calc(100% / 3);
  margin: 30px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
    0 2px 4px -1px rgba(0, 0, 0, 0.06);

  &__content {
    margin: 0 25px 0 25px;
  }

  &__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__title {
    font-weight: bold;
  }

  &__icon {
    height: 25px;
  }

  &__specificities {
    padding: 0;
  }

  &__specificity {
    list-style: none;
    display: flex;
    align-items: flex-end;
  }

  &__specificity:before {
    content: '';
    display: inline-block;
    height: 16px;
    width: 16px;
    background-image: url('../assets/images/picto_validate.svg');
    background-repeat: no-repeat;
    margin-right: 10px;
  }

  &__img {
    width: 100%;
    img {
      width: 100%;
    }
  }

  &__specificities {
    margin: 8px 0;
  }

  &__price {
    color: #6fd1cb;
    text-align: right;
    &-small {
      font-size: 0.7em;
    }
  }
}
</style>
