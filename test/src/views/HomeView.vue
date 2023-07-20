<template>
  <div>
    <h1>Welcome to {{title}} Home!</h1>
    <input type="text" v-model="input1" />
    <button type="button" @click="getData">Change</button>
    <button type="button" @click="setData">Set</button>

    <select class="form-control" v-model="Area" @change="changeReigon">
      <option :key="i" :value="d.v" v-for="(d,i) in options">{{d.t}}</option>
    </select>

    <table class="table table-bordered" v-if="tableShow">
      <tr :key="i" v-for="(d,i) in options">
        <td>{{d.v}}</td>
        <td>{{d.t}}</td>
      </tr>
    </table>


  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "개발자 박원지의",
      title2: "Daegu",
      input1: "abcd",
      options: [
        {v:"S",t:"Seoul"},
        {v:"J",t:"Jeju"},
        {v:"B",t:"Busan"},
        {v:"D",t:"Daegu"},
      ],
      region: "D",
      Area: "S",
      tableShow: false,
    };
  },
  watch: {
    input1(){
      // 데이터가 변동되는걸 캐치해서 알 수 있음(특정데이터를 계속 관찰하고 있다가 데이터가 변경 되었을 때 캐치해서 쓸수있음)
      console.log(this.input1);
    },
    title(){
      console.log(this.title)
    }
  },
  methods: {
    getData(){
      alert(this.input1)
    },
    setData(){
      this.input1 = "12345"
    },
    changeArea(){
      alert(this.Area)
    }
  },
  beforeCreate(){
    // console.log("beforeCreate")
  },
  created(){
    // console.log("created")
  },
  beforeMounted(){
    // console.log("beforeMounted")
  },
  mounted(){
    // console.log("mounted")
  },
  beforeUpdate(){
    // console.log("beforeUpdate")
  },
  updated(){
    // console.log("updated")
  },
  beforeDestroy(){
    // console.log("beforeDestroy")
  },
  destroyed(){
    // console.log("destroyed")
  }
}
</script>
