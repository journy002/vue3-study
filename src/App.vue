<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div>
    <h4>xx 원룸</h4>
    <p>{{ price1 }} 만원</p>
  </div>
  <div>
    <h4>xx 원룸</h4>
    <p>xx 만원</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      price1: "50",
    };
  },
  components: {},
};
</script>

<style></style>
