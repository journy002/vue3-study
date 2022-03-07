<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div>
    <h3>원룸샵</h3>
    <h4>{{ products[0] }}</h4>
    <p>{{ price1 }} 만원</p>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>{{ price2 }} 만원</p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>{{ price3 }} 만원</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      price1: "150",
      price2: "70",
      price3: "80",
      products: ["역삼동 원룸", "인덕원 원룸", "과천 원룸"],
    };
  },
  components: {},
};
</script>

<style></style>
