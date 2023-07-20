<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <h4>{{ nm1 }} 오피스텔</h4>
    <p>{{ price1 }} 만원</p>
  </div>
  <div>
    <h4>{{ nm2 }} 오피스텔</h4>
    <p>{{ price2 }} 만원</p>
  </div>
</template>

<script>

export default {
  name: 'App',
  //데이터바인딩을 위한 데이터 보관함
  data(){
    return {
      nm1: "원지",
      nm2: "세훈",
      price1: 68.7,
      price2: 80,
    }
  },
  components: {
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
