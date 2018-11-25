<template>
  <div class="header">
    <!-- 顶部通栏 -->
    <div class="top-wrapper">
      <div class="back-wrapper">
        <span class="iocn-arrow_lift"></span>
      </div>

      <form action="" class="search-wrapper">
        <span class="search-icon"></span>
        <input type="text" class="search-bar" placeholder="搜索店内商品">
      </form>

      <div class="more-wrapper">
        <a href="#" class="spelling-bt">拼单</a>
        <div class="more-bt">
          <i class="s-radius"></i>
          <i class="s-radius"></i>
          <i class="s-radius"></i>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {

  data () {
    return {
      
    }
  },
  props:{
    'poiInfo':{
      default:{}
    }
  },
  updated() {
    console.log(this.poiInfo)
  }
}
</script>

<style scoped>
  @import url(../../common/css/iocn.css);
  .header{
    padding-top: 28px;
  }
  .header .top-wrapper{
    position: relative;
  }
  .header .top-wrapper .back-wrapper{
    width: 50px;
    height:31px;
    position: absolute;
    left: 0;
    top: 0;
    text-align: center;
    line-height: 31px;
  }
  .header .top-wrapper .back-wrapper span{
    display: inline-block;
    color: #ffffff;
  }
  .header .top-wrapper .search-wrapper{
    width: 100%;
    height: 31px;
    background-attachment: pink;
    padding: 0 104px 0 50px;
    box-sizing: border-box;
  }
  .header .top-wrapper .search-wrapper .search-icon{
    width: 28px;
    height: 31px;
    background-size: 13px 13px;
    position: absolute;
  }
  .header .top-wrapper .search-wrapper .search-icon{
    width: 100%;
    height: 31px;
    box-sizing: border-box;
    background: #cdcdcc;
    border-radius: 25px;
    padding-left: 28px;
  }
</style>