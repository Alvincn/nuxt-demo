<template>
  <div class="blog">
    <!-- 这是头部导航栏 -->
    <div class="tabbar">
      <div id="logo">Alvin</div>
      <div>
        <el-button icon="el-icon-search" circle type="primary" size="mini"></el-button>
        <el-button icon="el-icon-setting" circle type="primary" size="mini"></el-button>
      </div>
    </div>
    <nuxt />
  </div>
</template>

<script>
</script>
<style>
.tabbar {
  width: 100vw;
  height: 40px;
  padding: 5px 10px;
  display: flex;
  line-height: 30px;
  justify-content: space-between;
  background-color: rgb(0, 200, 255);
}
</style>