<template>
  <section>
    <!-- <img src="@/assets/img/intro/mobile.svg" class="image intro-header" v-if="showMobile" alt="">
    <img src="@/assets/img/intro/wide-mobile.svg" class="image intro-header" v-if="showExtraMobile" alt="">
    <img src="@/assets/img/intro/touch.svg" class="image intro-header" v-if="showTouch" alt="">
    <img src="@/assets/img/intro/desktop.svg" class="image intro-header" v-if="showDesktop" alt="">
    <img src="@/assets/img/intro/widescreen.svg" class="image intro-header" v-if="showWidescreen" alt=""> -->
    <DesktopHeader v-if="showDesktop" /> 
    <WidescreenHeader v-if="showWidescreen" /> 
  </section>
</template>

<script>
import VueScreenSize from 'vue-screen-size'
import DesktopHeader from '@/assets/img/dentrofuera/desktop.svg'
import WidescreenHeader from '@/assets/img/dentrofuera/widescreen.svg'

export default {
  components:{
    DesktopHeader,
    WidescreenHeader
  },
  mixins: [VueScreenSize.VueScreenSizeMixin],
  computed: {
    showDesktop: function(){
      return this.$vssWidth > 0 && this.$vssWidth <= 1440
    },
    showWidescreen: function(){
      return this.$vssWidth > 1440
    },
  },
}
</script>

<style lang="scss" scoped>
.intro-header{
  width:100%;
  margin-bottom: 0;
}
section{
  line-height: 0;
}
</style>