<template>
  <div class="advantage">
    <p class="advantage__title">{{ advantage1.title }}</p>
    <div>
      <img class="advantage__img" :src="advantage1.img" alt="ok" />
    </div>
    <p class="advantage__desc">{{ advantage1.desc }}</p>
  </div>
</template>

<script>
export default {
  props: ['advantage1'],
}
</script>

<style lang="scss" scoped>
.advantage__img {
  height: 20px;
}
</style>
