<!-- layout -->
<template>
  <div>

    <heroTwo/>
    <gallerySample/>
    <galleryExamples/>
    <galleryFeatures/>

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
  import galleryFeatures from '@/components/galleryFeatures.vue'

  export default {
    name: 'home',
    components: { heroTwo, gallerySample, galleryExamples, galleryFeatures }
  }
</script>
