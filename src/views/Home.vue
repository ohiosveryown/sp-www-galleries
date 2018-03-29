<!-- layout -->
<template>
  <div>

    <heroTwo/>
    <gallerySample/>
    <galleryExamples/>

  </div>
</template>


<!-- style -->
<style lang="scss" scoped>

</style>


<!-- logic -->
<script>
  import heroTwo from '@/components/heroTwo.vue'
  import gallerySample from '@/components/gallerySample.vue'
  import galleryExamples from '@/components/galleryExamples.vue'

  export default {
    name: 'home',
    components: { heroTwo, gallerySample, galleryExamples }
  }
</script>
