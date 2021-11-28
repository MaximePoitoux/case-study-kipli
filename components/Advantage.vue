<template>
  <div class="advantage">
    <p class="advantage__title">{{ advantage.title }}</p>
    <img class="advantage__img" :src="advantage.img" :alt="advantage.title" />
    <p class="advantage__desc">{{ advantage.desc }}</p>
  </div>
</template>

<script>
export default {
  props: {
    advantage: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.advantage {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  width: calc(100% / 5);

  &__title {
    font-size: 1.2em;
  }

  &__img {
    height: 50px;
  }

  &__desc {
    height: 60px;
    text-align: center;
    font-size: 1em;
    width: 80%;
  }
}
</style>
