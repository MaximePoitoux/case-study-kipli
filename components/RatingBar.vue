<template>
  <div class="rating-bar">
    <img class="rating-bar__icon" src="../assets/images/star.svg" />
    <img class="rating-bar__icon" src="../assets/images/star.svg" />
    <img class="rating-bar__icon" src="../assets/images/star.svg" />
    <img class="rating-bar__icon" src="../assets/images/star.svg" />
    <img class="rating-bar__icon" src="../assets/images/star.svg" />
    <p class="rating-bar__desc">
      4,8/5 -
      <a href="#">Plus de 1594 avis</a>
    </p>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.rating-bar {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
  background-color: #f0f6ed;

  &__icon {
    height: 16px;
    margin: 2px;
  }

  &__desc {
    margin-left: 8px;

    a {
      color: #305157;
    }
  }
}
</style>
