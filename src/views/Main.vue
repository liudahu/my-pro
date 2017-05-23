<template>
  <div>
    <div class="list">
      <!--<muyin-->
        <!--v-for="item in muyinList"-->
        <!--:detail="item"-->
        <!--:data="item"-->
        <!--:key="item.name"></muyin>-->
      <!--<div style="float: left; width:436px">-->
        <!--<good-->
          <!--v-for="item in goodList"-->
          <!--:detail="item"-->
          <!--:data="item"-->
          <!--:key="item.name"></good>-->
      <!--</div>-->
      <div style="clear: both;width:800px;"><!--- 这里是商品 ---->
        <aa v-for="item in allitems"
            :itemIndex="item"
            :data="item"
            :key="item.describe" class="allitems" @upup="change" >
        </aa>
        <div class="shopping"><!-- 点击商品加入购物车后 把商品放到这个div里面 等于说是组件之间的传递--->

        </div>
      </div>

    </div>
  </div>
</template>
<style lang="less" rel="stylesheet/less">
  .list {
    padding: 10px;
  }
  .allitems{
    width:200px;
    display: inline-block;
  }
  .shopping{
    width:99%;
    border:1px solid red;
    height:500px;
  }

</style>
<script>
  import goodList from '../mock/goodLIst'
  import good from '../components/Good.vue'
  import muyin from '../components/muyin.vue'
  import aa from '../components/aa.vue' //aa是每个商品的组件
  import muyinList from '../mock/muyinList'
  import allitems from '../mock/allitems' //allitems是aa组件里面的虚拟数据

  export default {
    name: 'main',
    data () {
      return {
        goodList, muyinList,allitems,
//        msg
      }
    },
    methods: {
      change(msg){
        this.msg= msg;
      }
    },
    components: {
      good,
      muyin,
      aa
    }
  }
</script>
