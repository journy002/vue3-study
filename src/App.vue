<template>
  <div class="menu">
    <a v-for="(a, i) in menus" :key="i">{{ a }}</a>
  </div>
  <div>
    <h3>원룸샵</h3>
    <h4 v-for="item in products" :key="item">
      <b>{{ item.name }}</b
      >({{ item.price }})
    </h4>
  </div>
  <!-- <div>
    <h4>{{ products[1] }}</h4>
    <p>{{ price2 }} 만원</p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>{{ price3 }} 만원</p>
  </div> -->
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      price1: "150",
      price2: "70",
      price3: "80",
      menus: ["Home", "Shop", "About"],
      products: [
        { name: "역삼동원룸", price: "100만원" },
        { name: "인덕원원룸", price: "60만원" },
        { name: "과천원룸", price: "80만원" },
      ],
    };
  },
  components: {},
};
</script>

<style>
#app {
  text-align: center;
}
body {
  margin: 0 auto;
  padding: 0;
}
.menu {
  padding: 15px 10px;
  background-color: darkslateblue;
  border-radius: 5px;
}
.menu a {
  padding: 5px 10px;
  color: #ffffff;
}
</style>
