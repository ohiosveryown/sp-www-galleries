<!-- layout -->
<template>
  <div class="debug mw__lg">

    <div class="row">
      <div class="box">
        <div class="video-wrapper">
          <video width="100%" autoplay loop src="../assets/img/gallery.mp4"></video>
          <img class="pattern-03" src="../assets/img/01-waves.svg" alt="">
          <!-- <img class="pattern-04" src="../assets/img/02-waves.svg" alt=""> -->
        </div>
      </div>

      <article class="">
        <figure class="pattern-01">
          <img src="../assets/img/01-pattern.svg" alt="">
        </figure>
        <h1 class="mt-6 mb-3 f-lg f-sectra bold">Galleries that show your photos how they're supposed to be seen</h1>
        <p class="measure-8 f-graphik">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</p>

        <figure class="pattern-02">
          <img src="../assets/img/02-pattern.svg" alt="">
        </figure>
        <h1 class="mt-4 mb-3 f-lg f-sectra bold">Instantly deliver photos with digital downloads</h1>
        <p class="measure-8 f-graphik">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</p>

        <h1 class="mt-4 mb-3 f-lg f-sectra bold">Allow contacts to pick their favorite photos</h1>
        <p class="mb-9 measure-8 f-graphik">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</p>
      </article>
    </div>

  </div>
</template>


<!-- style -->
<style lang="scss" scoped>
  @import '../assets/style/grid.scss';

  .row {
    display: flex;
    padding-top: calc(var(--unit) * 24);
  }

  .box {
    width: grid-width(6);
    height: 60vh;
    margin-right: 4rem;
    background: rgba(0,0,0,0);

    position: sticky;
    position: -webkit-sticky;
    top: calc(var(--unit) * 24);
  }

  .video-wrapper {
    position: relative;
  }

  video {
    box-shadow: 0px 41px 61px -28px rgba(0,0,0,0.3);
  }

  article {
    position: relative;
    padding: 2.4rem 1.6rem;
    width: grid-width(6);

    p:nth-of-type(1), p:nth-of-type(2) { margin-bottom: 72rem; }
    p:nth-of-type(3) { margin-bottom: 20rem; }
  }

  .pattern-01 {
    position: absolute;
    top: 4rem; left: 0rem;
    z-index: var(--zmin);
  }

  .pattern-02 {
    position: absolute;
    top: 95rem; left: 0rem;
    z-index: var(--zmin);
  }

  .pattern-03 {
    position: absolute;
    bottom: -6rem; left: -6rem;
    z-index: var(--zmin);
  }

  .pattern-04 {
    position: absolute;
    top: -6rem; right: -6rem;
    z-index: var(--zmin);
  }

</style>


<!-- logic -->
<script>
  export default { name: 'gallerySample' }
</script>
