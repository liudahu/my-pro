<template>
  <div>
    <div class="list">
      <muyin
             v-for="item in muyinList"
             :detail="item"
             :data="item"
             :key="item.name"></muyin>
      <div style="float: left; width:436px">
      <good
            v-for="item in goodList"
            :detail="item"
            :data="item"
            :key="item.name"></good>
        </div>
        </div>
  </div>
</template>
<style lang="less" rel="stylesheet/less">
.list{
  padding:10px;
}

</style>
<script>
  import goodList from '../mock/goodLIst'
  import good from '../components/Good.vue'
  import muyin from '../components/muyin.vue'
  import muyinList from '../mock/muyinList'

  export default {
    name: 'main',
    data () {
      return {
        goodList,muyinList
      }
    },
    components: {
      good,
      muyin
    }
  }
</script>
