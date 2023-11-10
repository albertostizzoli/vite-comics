<template>
  <AppHeader />
  <AppContent />
  <FooterTop />
  <FooterMiddle />
  <FooterBottom />
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import FooterTop from './components/FooterTop.vue';
import FooterMiddle from './components/FooterMiddle.vue';
import FooterBottom from './components/FooterBottom.vue';
export default {
  name: 'App',
  components: {
    AppHeader,
    AppContent,
    FooterTop,
    FooterMiddle,
    FooterBottom
  },
}
</script>

<style lang="scss"></style>
