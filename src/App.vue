<script>
  import AppNav from './components/AppNav.vue';

export default {
  components: {
    AppNav,
  }
}
</script>

<template>
  <div id="container">
    <AppNav></AppNav>
  </div>
</template>

<style lang="scss">
  @use './style/variables' as *;
  @use './style/mixins' as *;

  #container {
    @include centered;
  }

</style>
