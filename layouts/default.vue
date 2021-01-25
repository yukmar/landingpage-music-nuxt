<template>
  <div id="app">
    <Header />
    <transition name="fade">
      <Nuxt />
    </transition>
    <Footer v-if="checkUrl" />
    <div id="circle-1"></div>
    <div id="circle-2"></div>
    <div id="circle-3"></div>
  </div>
</template>
<script>
export default {
  computed: {
    checkUrl() {
      console.log(this.$route.name)
      return this.$route.name !== 'index'
    },
  },
}
</script>
<style lang="scss" scoped>
.fade-enter,
.fade-leave-to {
  opacity: 0;
  transform: translateX(2rem);
}
.fade-enter-active,
.fade-leave-active {
  transition: all 0.3s ease;
}

#circle-1 {
  @include circle(16em, 16em, #3c313f, 50%, bottom, 3em, left, 6em);
}

#circle-2 {
  @include circle(10em, 10em, #2f3446, 50%, top, 13vh, left, 40vw);
}

#circle-3 {
  @include circle(30em, 30em, #2d364f, 50%, bottom, 0, right, 0);
  transform: translate(40%, 40%);
}
</style>
