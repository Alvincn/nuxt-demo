<template>
  <div>
    {{ goodsId }}
  </div>
</template>

<script lang='ts'>
import Vue from 'vue'

export default Vue.extend({
  name: 'GoodsId',
  data() {
    return {
      goodsId: ''
    }
  },
  mounted() {
    console.log(this.$route);
    this.goodsId = this.$route.params.id
  }
})
</script>

<style></style>