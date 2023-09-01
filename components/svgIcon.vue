<template>
  <div>
    <img :src="require(`~/assets/svg/${svgName}.svg`)" :style="{ width, height }" />
  </div>
</template>

<script lang='ts'>
import Vue from 'vue'
export default Vue.extend({
  name: 'SvgIcon',
  props: {
    width: {
      default: '200px',
      type: String
    },
    height: {
      default: "200px",
      type: String
    },
    svgName: {
      required: false,
      type: String,
    },
  }
})
</script>