<template>
  <div class="pt_cover">
    <a href="">
      <img class="pt_cover_img" :src="detail.pic"/>
    </a>
  </div>
</template>
<style lang="less" rel="stylesheet/less">

  .pt_cover{
    float: left;
    width: 150px;
    height: 260px;
    overflow: hidden;
    margin-right: 10px;
    background-color: #f7f7f7;
    a{
      .pt_cover_img {
        position:relative;
        left:0;
        right:0;
        display: block;
        width: 193px;
        height: 260px;
        transition: all .5s linear;

      }

    }
  }
  .pt_cover :hover .pt_cover_img {
    left:-10px;
  }
</style>
<script>
  export default {
    name: 'muyin',
    props: ['detail']
  }
</script>
