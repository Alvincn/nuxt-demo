<template>
  <div class="manager">
    <!-- 这是头部导航栏 -->
    <div class="tabbar">
      <div id="logo">后台管理系统</div>
      <div class="icon-setting">
        <el-button icon="el-icon-search" circle type="primary" size="mini"></el-button>
        <el-button icon="el-icon-setting" circle type="primary" size="mini"></el-button>
      </div>
    </div>
    <div class="context">
      <div class="menu">
        <el-menu default-active="1-4-1" class="el-menu-vertical-demo" @open="handleOpen" @close="handleClose"
          :collapse="isCollapse">
          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span slot="title">用户管理</span>
            </template>
            <el-menu-item-group>
              <span slot="title">商品管理</span>
              <el-menu-item index="1-1">选项1</el-menu-item>
              <el-menu-item index="1-2">选项2</el-menu-item>
            </el-menu-item-group>
            <el-menu-item-group title="分组2">
              <el-menu-item index="1-3">选项3</el-menu-item>
            </el-menu-item-group>
            <el-submenu index="1-4">
              <span slot="title">选项4</span>
              <el-menu-item index="1-4-1">选项1</el-menu-item>
            </el-submenu>
          </el-submenu>
          <el-menu-item index="2">
            <i class="el-icon-menu"></i>
            <span slot="title">订单管理</span>
          </el-menu-item>
          <el-menu-item index="4">
            <i class="el-icon-setting"></i>
            <span slot="title">设置</span>
          </el-menu-item>
        </el-menu>
      </div>
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isCollapse: false
    };
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>
<style lang="less">
.tabbar {
  width: 100vw;
  height: @tabbar-height;
  padding: 5px 10px;
  display: flex;
  line-height: calc(@tabbar-height - 10px);
  font-size: @font-size-small;
  font-weight: 800;
  justify-content: space-between;
  background-color: rgb(0, 200, 255);
  .icon-setting {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}

.manager {
  width: 100%;
  height: calc(100vh - @tabbar-height);
}

.menu {
  width: @menu-width;
  height: calc(100vh - @tabbar-height);
}

.context {
  display: flex
}
</style>