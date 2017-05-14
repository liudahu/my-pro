<template>
  <div class="item">
    <div class="Goodleft">
      <i>{{detail.name}}</i>
      <span>{{detail.price}}</span>
    </div>
    <img :src="detail.pic" class="GoodRight"/>
  </div>

</template>
<style>
.item{
  /*width:350px;*/
  display: inline-block;
}
i,span{
  display: block;
  background: hsla(0,0%,100%,.8);
}
.Goodleft,.GoodRight{
  display: inline-block;
}
.Goodleft{
  vertical-align: top;
  position:relative;
  z-index: 2;
}
.GoodRight{
  position:relative;
  left:-15px;
  transition: all 0.5s linear;
  z-index: 1;
}
.GoodRight:hover{
  left:-25px;
}
</style>
<script>
  export default {
    name: 'good',
    props: ['detail']
  }
</script>
