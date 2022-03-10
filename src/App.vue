<template>
  <div class="menu">
    <a v-for="(a, i) in menus" :key="i">{{ a }}</a>
  </div>
  <div>
    <h3>원룸샵</h3>
    <!--  반복문 사용 방법
      <h4 v-for="item in products" :key="item">
      <b>{{ item.name }}</b
      >({{ item.price }})
    </h4> -->
  </div>
  <div>
    <img src="./assets/room0.jpg" alt="" class="room-img" />
    <h4>{{ products[0].name }}</h4>
    <p>{{ price1 }} 만원</p>
    <button @click="count[0]++">허위 신고 매물</button
    ><span>신고수 : {{ count[0] }}</span>
  </div>
  <div>
    <img src="./assets/room1.jpg" alt="" class="room-img" />
    <h4>{{ products[1].name }}</h4>
    <p>{{ price2 }} 만원</p>
    <button @click="count[1]++">허위 신고 매물</button
    ><span>신고수 : {{ count[1] }}</span>
  </div>
  <div>
    <img src="./assets/room2.jpg" alt="" class="room-img" />
    <h4>{{ products[2].name }}</h4>
    <p>{{ price3 }} 만원</p>
    <button @click="count[2]++">허위 신고 매물</button
    ><span>신고수 : {{ count[2] }}</span>
  </div>
</template>

<script>
export default {
  name: "App",
  // vue에서 data를 만들어서 사용하고 싶을때
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
      count: [0, 0, 0],
    };
  },

  // 함수를 만들어서 사용하고 싶을때
  // vue에서 함수를 만들때 함수안에서 data값을 가져와 사용하고 싶으면 앞에 꼭 this를 사용해서 내 오브잭트에서 데이터를 사용하겠다 라고 알려줘야한다.
  methods: {},
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

.room-img {
  margin: 0 3px;
  width: calc(100% - 300px);
}
</style>
