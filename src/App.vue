<!-- layout -->
<template>
  <div id="app">
    <!-- <div>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->

    <navigation class="mw__lg" />
    <router-view/>
  </div>
</template>


<!-- style -->
<style lang="scss">
  @import './assets/style/reset.scss';

</style>


<!-- logic -->
<script>
  import navigation from '@/components/navigation.vue'

  export default {
    components: { navigation }
  }
</script>
