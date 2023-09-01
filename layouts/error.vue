<template>
  <div class="container">
    <h1 v-if="error.statusCode === 404">
    </h1>
    <div class="notfind">
      <svg-icon svgName="404" width="400px" height="400px"></svg-icon>
      <h4>您访问的页面不存在！</h4>
    </div>
  </div>
</template>

<script lang='ts'>


export default {
  props: ['error'],
  layout: 'manager',
}
</script>

<style scoped lang="less">
.container {
  width: 100%;
  height: 100%;
}
.notfind {
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>