<!-- layout -->
<template>
  <div>

    <heroTwo/>
    <gallerySample/>

  </div>
</template>


<!-- style -->
<style lang="scss" scoped>

</style>


<!-- logic -->
<script>
  import heroTwo from '@/components/heroTwo.vue'
  import gallerySample from '@/components/gallerySample.vue'

  export default {
    name: 'home',
    components: { heroTwo, gallerySample }
  }
</script>
