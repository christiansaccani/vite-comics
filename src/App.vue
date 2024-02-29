<script>
  import AppNav from './components/AppNav.vue';
  import AppContent from './components/AppContent.vue';
  import AppMedia from './components/AppMedia.vue'

export default {
  components: {
    AppNav,
    AppContent,
    AppMedia,
  }
}
</script>

<template>
  <div id="container">
    <AppNav></AppNav>
    <AppContent></AppContent>
    <AppMedia></AppMedia>
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
