<template>
  <div class="vue_det">
    <h1>{{ msg }}</h1>

    <div v-html="message"/>

    <label for="r1">修改颜色</label><input type="checkbox" v-model="class1" id="r1">

    <br><br>
    <div v-bind:class="{'class1': class1}">
      <p>v-bind:class 指令</p>
    </div>

  </div>
</template>

<script>
  export default {
    data () {
      return {
        msg: '非常 非常欢迎您!!',
        message: '<h1>菜鸟教程111</h1>',
        class1: true
      }
    },
    methods: {
      details: function() {
        return  this.site + " - 学的不仅是技术，更是梦想！";
      }
    }
  }
</script>

<style scoped>

  p {
    color: #42b983;
  }
</style>
