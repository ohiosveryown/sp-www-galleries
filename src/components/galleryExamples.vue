<!-- layout -->
<template>
  <div>
    <!-- <div class="lightbox">
      <div class="lightbox__content mw__lg">

      </div>
    </div> -->

    <section style="min-height: 100vh;" class="mw__lg">

      <div class="title__wrapper">
        <h1 class="mb-2 f-xl f-sectra bold jc">Beautiful Galleries</h1>
        <p class="f-graphik jc">Duis aute irure dolor in reprehenderit in voluptate cillum dolore eu fugiat nulla pariatur.<br>Excepteur sint occaecat cupidatat non proident velit esse enim.</p>
      </div>

      <div class="mt-9 row">
        <div class="example-list">
          <h2 class="mb-2 f-md f-graphik bold uc">examples</h2>
          <hr class="mb-2">
          <ul class="f-sm f-graphik">
            <li class="mb-1">Newborn</li>
            <li class="mb-1">Seniors</li>
            <li class="mb-1">Wedding</li>
            <li class="mb-1">Portrait</li>
            <li>Sports</li>
          </ul>
        </div>

        <div class="galleries">
          <article class="">
            <figure class="gallery-01 mb-3">
              <div class="gallery-hover">
                <div class="gallery-hover__content">
                  <button class="tigger f-sm f-graphik bold uc">choose this template</button>
                  <a class="f-sm f-graphik bold uc" href="#">preview gallery</a>
                </div>
              </div>
            </figure>
            <h5 class="mb-1 f-sm f-graphik bold uc">sample gallery with autoplay music</h5>
            <p class="f-graphik">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et.</p>
          </article>

          <article class="">
            <figure class="gallery-02 mb-3">
              <div class="gallery-hover">
                <div class="gallery-hover__content">
                  <button class="f-sm f-graphik bold uc">choose this template</button>
                  <a class="f-sm f-graphik bold uc" href="#">preview gallery</a>
                </div>
              </div>
            </figure>
            <h5 class="mb-1 f-sm f-graphik bold uc">sample gallery with paid digitals</h5>
            <p class="f-graphik">Duis aute irure dolor in reprehenderit in voluptate cillum dolore eu fugiat nulla pariatur.</p>
          </article>

          <article class="">
            <figure class="gallery-03 mb-3">
              <div class="gallery-hover">
                <div class="gallery-hover__content">
                  <button class="f-sm f-graphik bold uc">choose this template</button>
                  <a class="f-sm f-graphik bold uc" href="#">preview gallery</a>
                </div>
              </div>
            </figure>
            <h5 class="mb-1 f-sm f-graphik bold uc">Sample with Autoplay Music – Slideshow only</h5>
            <p class="f-graphik">Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi aliquip ex ea commodo.</p>
          </article>

          <article class="">
            <figure class="gallery-04 mb-3">
              <div class="gallery-hover">
                <div class="gallery-hover__content">
                  <button class="f-sm f-graphik bold uc">choose this template</button>
                  <a class="f-sm f-graphik bold uc" href="#">preview gallery</a>
                </div>
              </div>
            </figure>
            <h5 class="mb-1 f-sm f-graphik bold uc">sample gallery with free digitals</h5>
            <p class="f-graphik">Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim.</p>
          </article>

          <article class="">
            <figure class="gallery-05 mb-3">
              <div class="gallery-hover">
                <div class="gallery-hover__content">
                  <button class="f-sm f-graphik bold uc">choose this template</button>
                  <a class="f-sm f-graphik bold uc" href="#">preview gallery</a>
                </div>
              </div>
            </figure>
            <h5 class="mb-1 f-sm f-graphik bold uc">Sample with Autoplay Music</h5>
            <p class="f-graphik">Duis aute irure dolor in reprehenderit in voluptate cillum dolore eu fugiat nulla pariatur.</p>
          </article>

          <article class="">
            <figure class="gallery-06 mb-3">
              <div class="gallery-hover">
                <div class="gallery-hover__content">
                  <button class="f-sm f-graphik bold uc">choose this template</button>
                  <a class="f-sm f-graphik bold uc" href="#">preview gallery</a>
                </div>
              </div>
            </figure>
            <h5 class="mb-1 f-sm f-graphik bold uc">sample gallery with paid digitals</h5>
            <p class="f-graphik">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et.</p>
          </article>
        </div>
      </div>

    </section>
  </div>
</template>


<!-- style -->
<style lang="scss" scoped>
  @import '../assets/style/grid.scss';

  .lightbox {
    position: fixed;
    top: 0; left: 0;
    width: 100vw; height: 100vh;
    z-index: var(--zmin);
    background: rgba(37,38,39,.93);
    opacity: 0.2;
    transition: var(--ease);
  }

  .active {
    z-index: var(--zmax);
    opacity: 1;
  }

  .lightbox__content {
    position: relative;
    border: 2px solid red;
    height: 100%;
  }

  section { margin-top: 11.2rem; }

  .title__wrapper {
    position: relative;
    margin: 0 auto 0 27rem;
    width: 64%;
  }

  .row {
    display: flex;
    min-height: 200vh;
    width: grid-width(12);
    padding-top: calc(var(--unit) * 1);
  }

  .example-list {
    position: sticky;
    position: -webkit-sticky;
    top: calc(var(--unit) * 24);
    width: grid-width(2); height: 20rem;
  }

  hr {
    border: .5px solid #d6d6d6;
  }

  ul {
    display: flex;
    flex-direction: column;
  }

  .galleries {
    width: grid-width(12);
    display: flex;
    flex-wrap: wrap;
  }

  article {
    // position: relative;
    padding: 0 4rem 2rem 4rem;
    width: grid-width(6);
  }

  figure {
    position: relative;
    margin-top: 2rem;
    width: 100%; height: 300px;
    border: 1px solid lightgray;
    border-radius: 4px;
  }

  .gallery-01 {
    background: url('../assets/img/01-gallery.png') no-repeat center center;
    background-size: cover;
  }

  .gallery-02 {
    background: url('../assets/img/02-gallery.png') no-repeat center center;
    background-size: cover;
  }

  .gallery-03 {
    background: url('../assets/img/03-gallery.png') no-repeat center center;
    background-size: cover;
  }

  .gallery-04 {
    background: url('../assets/img/04-gallery.png') no-repeat center center;
    background-size: cover;
  }

  .gallery-05 {
    background: url('../assets/img/05-gallery.png') no-repeat center center;
    background-size: cover;
  }

  .gallery-06 {
    background: url('../assets/img/07-gallery.png') no-repeat center center;
    background-size: cover;
  }

  figure >.gallery-hover { opacity: 0; }
  figure:hover > .gallery-hover { opacity: 1; }

  .gallery-hover {
    position: absolute;
    top: 0; left: 0;
    transition: all 300ms ease;
    width: 100%; height: 100%;
    background: rgba(255,255,255,0.9);

    &:hover { transition: all 400ms ease 100ms; }
  }

  .gallery-hover__content {
    width: 100%; height: 100%;
    margin-top: 1rem;
    display: flex;
    flex-direction: column;
    text-align: center;
    justify-content: center;
    align-items: center;

    button {
      margin-bottom: 2rem;
      padding: 1.2rem 2rem;
      border-radius: 4px;
      background: #031FBF;
      color: #fff;
    }
  }

</style>


<!-- logic -->
<script>
  export default {
    name: 'galleryExamples',

    // mounted() {
    //   const trigger = document.querySelector('.trigger');
    //
    //   trigger.addEventListener('click', () => {
    //     document.querySelector('.lightbox').classList.add('active')
    //   });
    // }
  }
</script>
