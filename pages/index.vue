<template>
  <div>
    <nuxt-link to="/user">用户</nuxt-link>
    <nuxt-link to="/goods/1">商品</nuxt-link>
    <el-button>默认按钮</el-button>
  </div>
</template>

<script lang='ts'>
import Vue from 'vue'

export default Vue.extend({
  name: 'Index',
  layout: 'manager',
  data() {
    return {
      keyDownArr: 'chenshiboyyds'.split(''),
      index: 0,
      timer: 2000
    }
  },
  mounted() {
    this.listenKeyDown()
  },
  methods: {
    listenKeyDown() {
      let timer: any = null
      document.body.addEventListener('keydown', (e) => {
        if (timer !== null) {
          clearTimeout(timer)
        }
        timer = setTimeout(() => {
          this.index = 0
        }, this.timer);
        if (e.key === this.keyDownArr[this.index]) {
          this.index++
        } else {
          this.index = 0
        }
        if (this.index === this.keyDownArr.length) {
          this.index = 0
          this.$router.push('/user')
        }
      })
    }
  }
})
</script>

<style></style>