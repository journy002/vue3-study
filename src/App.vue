<template>
  <!-- 모달 -->
  <div class="black-bg" v-if="modal_st == true">
    <div class="white-bg">
      <h4>상세 페이지</h4>
      <p>상세페이지 내용</p>
      <button @click="modal_st = false">닫기</button>
    </div>
  </div>

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
    <button @click="modal_st = true">상세 보기</button>
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
      modal_st: false,
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
  margin: 0;
  padding: 0;
}

/* 모달[S] */

div {
  box-sizing: border-box;
}

.black-bg {
  position: fixed;
  padding: 20px;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.white-bg {
  padding: 20px;
  width: 100%;
  background-color: #ffffff;
  border-radius: 8px;
}

/* 모달[E] */

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
