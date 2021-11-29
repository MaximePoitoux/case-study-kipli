<template>
  <button class="btn" :type="type">{{ text }}</button>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.btn {
  cursor: pointer;
  margin-top: 10px;
  padding: 10px;
  font-size: 1em;
  background-color: #b85e4c;
  color: white;
  border: none;
}
</style>
