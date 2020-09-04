<template>
  <div class="hello">
    <el-badge :value="12" class="item" :max="9" :hidden="ishidden">
      <el-button size="small">评论</el-button>
    </el-badge>
    <!-- <el-badge is-dot class="item">数据查询</el-badge>
    <el-badge is-dot class="item">
      <el-button class="share-button" icon="el-icon-share" type="primary"></el-button>
    </el-badge>
    <el-badge value="new" class="item">
      <el-button size="small">评论</el-button>
    </el-badge>
    <el-badge value="hot" class="item">
      <el-button size="small">回复</el-button>
    </el-badge> -->
  </div>
</template>

<script>
import IdBadge from '@/components/idBadge'
export default {
  name: "HelloWorld",
  data(){
    return{
      msg:"欢迎吴彦祖"
    }
  },

  component:{
    IdBadge
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
