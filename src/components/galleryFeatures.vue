<!-- layout -->
<template>
    <section>

      <div class="features">
        <div class="features__wrapper mw__lg">
          <div class="mt-8 features__list">
            <h2 class="mb-2 f-lg f-sectra bold">Gallery Features List</h2>
            <p class="mb-3 f-graphik">With automatic emails and custom email templates, keeping in touch with your clients (and potential clients) is a snap.</p>
            <ul class="f-graphik f-md">
              <li>•  Music that autoplaysss<span class="ml-8">•  Much profit</span></li>
              <li>•  Digitals that download<span class="ml-8">•  Sales, sales, sales</span></li>
              <li>•  Galleries that popssss<span class="ml-8">•  Such photo</span></li>
              <li>•  Sales, sales, sales</li>
              <li>•  Much profit</li>
              <li>•  Such wow</li>
            </ul>
          </div>
        </div>
        <div class="video__wrapper">
          <img class="play-btn" src="../assets/img/play.svg" alt="">
          <div class="cover"></div>
          <video width="100%" autoplay loop src="../assets/img/story-d.mp4"></video>
        </div>
      </div>

      <div class="sign-up">
        <div class="sign-up__wrapper mw__lg">
          <h1 class="mb-2 f-xl f-sectra bold">Try if free for 30 days</h1>
          <p class="f-graphik">No credit card is required, and if you’re not satisfied, call and ask for Robert Swarthout or Colin Breece.</p>
          <button class="f-sm f-graphik bold uc">get started</button>
        </div>
        <div class="sign-up__block"></div>
      </div>

      <footer>
        <span class="op-5 f-md f-graphik bold uc">footer</span>
      </footer>

    </section>
</template>


<!-- style -->
<style lang="scss" scoped>
  @import '../assets/style/grid.scss';

  section {
    margin-top: 19.6rem;
  }

  .features {
    width: 100%; min-height: 64rem;
    background: #e3ecff;
    display: flex;
    position: relative;
  }

  .features__list {
    padding-right: 6rem;
    width: grid-width(6);
  }

  .video__wrapper {
    position: absolute;
    top: -6rem; right: 0;
    z-index: var(--zmax);
    width: grid-width(5);
  }

  .video__wrapper:after {
    content: '';
    position: absolute;
    top: 24px; left: -24px;
    width: 100%; height: 100%;
    z-index: var(--zmin);
    background: #fff;
  }

  video {
    position: relative;
    box-shadow: 0 0 61px -28px rgba(0,0,0,0.05);
  }

  .play-btn {
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    z-index: var(--zmax);
    transition: var(--ease);
    cursor: pointer;
    &:hover { transform: translate(-50%, -50%) scale(1.3); }
  }

  .cover {
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 98%;
    background: rgba(0,0,0,0.5);
    z-index: var(--z2);
  }

  ul {
    list-style-type: circle;
  }

  ul > li {
    display: block;
    margin-bottom: 1.4rem;
    margin-left: 0.4rem;
  }

  .sign-up {
    position: relative;
  }

  .sign-up__wrapper {
    position: relative;
    z-index: var(--z3);
    width: 50%;
    text-align: center;
    transform: translateY(-8rem);

    p { width: 80%; position: relative; margin: 0 auto; }
  }

  .sign-up__block {
    position: absolute;
    top: -19.2rem; left: 0;
    z-index: var(--z2);
    width: 94%; height: 40rem;
    background: #fff;
  }

  button {
    margin-top: 3rem;
    padding: 1.2rem 4rem;
    border-radius: 4px;
    background: #031FBF;
    color: #fff;
  }

  footer {
    position: relative;
    width: 100vw; height: 48rem;
    background: red;
    z-index: var(--zmin);
    margin-top: -20rem;
    background: #f7f7f7;

    display: flex;
    justify-content: center;
    align-items: center;

    span { margin-top: 16.4rem; }
  }

</style>


<!-- logic -->
<script>
  export default { name: 'galleryFeatures' }
</script>
