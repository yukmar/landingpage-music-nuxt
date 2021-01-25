<template>
  <div :style="layoutCss" :class="baseStyle()">
    <slot></slot>
  </div>
</template>
<script>
export default {
  props: {
    layoutCss: {
      type: Object,
      default: null,
    },
    layoutClass: {
      type: Array,
      default: null,
    },
  },
  methods: {
    baseStyle() {
      const styleList = ['base-content']
      if (this.layoutClass) {
        styleList.push(...this.layoutClass)
      }
      return styleList
    },
  },
}
</script>
<style lang="scss" scoped>
.base-content {
  @apply flex flex-col flex-grow;
  @screen sm {
    @apply flex-row
      justify-around 
      p-0 w-4/5
      text-white;
  }
}
</style>
