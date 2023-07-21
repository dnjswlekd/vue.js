<template>

  <div class="menu">
    <a v-for="navbar in menus" :key="navbar">{{ navbar }}</a>
  </div>

  <!-- modal -->
  <div class="black-bg" v-if="openModal == true">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p>상세페이지 내용임</p>
      <button @click="openModal = 0">닫기</button>
    </div>
  </div>


  <!-- 반복문 -->
  <img alt="Vue logo" src="./assets/logo.png">
  <div v-for="(consturction,i) in logo" :key="i">
    <h1>{{ consturction }}</h1>
    <h4 class="red" :style="style">{{ nm[i] }} 오피스텔</h4>
    <p>{{ price[i] }} 만원</p>
    <p @click="openModal = true">{{ products[i] }}</p>
    <button @click="increase">허위매물신고</button><span> 신고수 : {{ 신고수 }}</span>
  </div>
  <!-- <div>
    <h4 :style="style1">{{ nm2 }} 오피스텔</h4>
    <p>{{ price2 }} 만원</p>
    <p>{{ products[2] }}</p>
  </div> -->


  <input v-model="wonji">
  <p>name: {{ nm2 }}</p>
</template>

<script>

export default {
  name: 'App',
  //데이터바인딩을 위한 데이터 보관함
  data(){
    return {
      nm1: "wonji",
      nm2: "sahun",
      openModal: false,
      신고수: 0,
      nm: ["원지", "세훈"],
      price: ["68.7", "80"],
      logo: ["원지네 부동산", "세훈이네 부동산"],
      style: "color: green",
      style1: "color: blue",
      products: ["신도림", "범어", "개봉"],
      menus: ["Home", "Shop", "Products", "About"]
    }
  },
  components: {
    
  },
  methods: {
    increase(){
      this.신고수++;
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  width: 20%;
  margin: 0 auto;
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}

body {
  margin: 0;
}

div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 500px; height: 500px;
  background: white;
  border-radius: 8px;
  padding: 20px;
  margin: 0 auto;
}
</style>
