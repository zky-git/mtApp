<template>
  <div class="nav">
    <router-link to="/goods" class="nav-item">
      点菜
      <i class="line"></i>
    </router-link>
    <router-link to="/ratings" class="nav-item">
      评价<span v-if="commentNum">({{commentNum}})</span>
      <i class="line"></i>
    </router-link>
    <router-link to="/seller" class="nav-item">
      商家
      <i class="line"></i>
    </router-link>
  </div>
</template>

<script>
export default {

  data () {
    return {
      
    }
  },
  props:{
    commentNum:{
      type:Number,
      default:0
    }
  }
}
</script>

<style scoped>
  .nav{
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 40px;
    border-bottom: 1px solid #e4e4e4;
  }
  .nav-item{
    flex: 1;
    text-align: center;
    font-size: 13px;
    color: #666;
    text-decoration: none;
    line-height: 40px;
    position: relative;
  }
  /* 选中的样式 */
  .nav .active{
    color: #ffbb22;

  }
  /* 选中下面的下划线 */
  .nav .active .line{
    height: 2px;
    width: 20px;
    display: inline-block;
    background: #ffbb22;
    position: absolute;
    left: 50%;
    margin-left:-10px;
    bottom: 0; 
  }
</style>