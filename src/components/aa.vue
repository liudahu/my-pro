<template>
  <div class="newItem">
    <img :src="itemIndex.dd" alt="">
    <p>{{itemIndex.describe}}</p>
    <p><span style="color:red">{{itemIndex.price}} 优惠价</span><span>{{itemIndex.oldprice}}</span></p>
    <span class="btn" @click="up">加入购物车</span>
  </div>
</template>
<style>
  .btn{
    width:150px;
    border-radius: 3px;
    color:#fff;
    height:40px;
    line-height:40px;
    background:red;
    font-weight:bold;
    cursor: pointer;
    text-align: center;
  }
</style>

<script>
  export default {
    name: 'aa',
//    data(){
//      itemIndex={};
//    },
    props: ['itemIndex'],
    methods: {
      up(){
        this.$emit('upup',itemIndex)
      }
    }
  }
</script>
