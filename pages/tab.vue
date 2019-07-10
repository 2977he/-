<template>
<div>
  <div class="ctr1">
    <span v-for="(item,index) in ['新闻','体育','军事']" :key="index" @click="handleClick(index)" :class="{active:current===index}">
        {{item}}
    </span>
    
  </div>
  <div v-if="current===0">
   <ul>宋仲基离婚</ul>
   <ul>宋仲基离婚</ul>
   <ul>宋仲基离婚</ul>
  </div>
  <div v-if="current===1">
      <ul>蔡徐坤打篮球</ul>
      <ul>蔡徐坤打篮球</ul>
      <ul>蔡徐坤打篮球</ul>
  </div>
  <div v-if="current===2">
      <ul>落地98K</ul>
      <ul>落地98K</ul>
      <ul>落地98K</ul>
  </div>
  </div>
</template>

<script>


export default {
  data(){
      return{
          current:0
          // 默认的显示的状态，第一个
      }
  },
  methods:{
        handleClick(index){
            this.current=index
        }
      }
}
</script>

<style>
 .crt1{
     margin-bottom: 10px
 }
 .crt1 span{
     cursor: pointer;
     margin:0 10px;
 }
 .active{
     color:aqua
 }
</style>
