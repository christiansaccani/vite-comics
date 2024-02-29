<script>
  import AppNav from './components/AppNav.vue';
  import AppContent from './components/AppContent.vue';

export default {
  components: {
    AppNav,
    AppContent,
  }
}
</script>

<template>
  <div id="container">
    <AppNav></AppNav>
    <AppContent></AppContent>
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
