<template>
  <div class="hello">
   <a v-bind:href="url">{{msg}}</a>
    <button @click="handle">切换</button>
    <form>
    <select v-model="occu">
     <option value="0">请选择职业</option>
      <option value="1">学生</option>
      <option value="2">老师</option>
      <option value="3">院长</option>
      <option value="4">校长</option>
    </select>

      <input type="submit" value="提交" @click.prevent="change1">
    </form>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: '百度',
      url:'http://www.baidu.com',
      occu:'1',
    }
  },
  methods:{
    handle:function () {
      this.msg="黑马";
      this.url='http://itcast.cn'
    },
    change1:function () {
        console.log(this.occu);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
