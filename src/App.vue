<script>
  import AppNav from './components/AppNav.vue';
  import AppContent from './components/AppContent.vue';
  import AppMedia from './components/AppMedia.vue';
  import AppLinks from './components/AppLinks.vue';
  import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppNav,
    AppContent,
    AppMedia,
    AppLinks,
    AppFooter,
  }
}
</script>

<template>
  <div id="container">
    <AppNav></AppNav>
    <AppContent></AppContent>
    <AppMedia></AppMedia>
    <AppLinks></AppLinks>
    <AppFooter></AppFooter>
  </div>
</template>

<style lang="scss">
  @use './style/variables' as *;
  @use './style/mixins' as *;

  #container {
    @include centered;

    display: flex;
    flex-flow: column nowrap;
    align-items: center;
  }

</style>
