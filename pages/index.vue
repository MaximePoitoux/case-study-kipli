<template>
  <div>
    <RatingBar />
    <div class="landing">
      <div class="landing__title">
        <p>Pour les professionnels <br />et l'hôtellerie</p>
      </div>
      <Form />
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
  height: 650px;
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
    }
  }
}
</style>
