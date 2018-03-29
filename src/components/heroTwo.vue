<!-- layout -->
<template>
  <div class="bg">

    <section class="mw__lg">
      <div class="intro">
        <!-- headline -->
        <h1 class="fade-in mb-4 f-xl f-sectra bold">See how ShootProof Galleries can make photograpy better and brighter.</h1>
        <!-- intro copy -->
        <p class="fade-in measure-6 mb-6 f-graphik">Galleries are a single space for creating and sharing together. Work seamlessly with all types of photos—from weddings and portrait, to seniors and newborns.</p>
        <!-- button -->
        <div class="fade-in question-link">
          <a><h4 class="f-sm f-graphik bold">See Susan's Gallery</h4></a>
        </div>
      </div>
    </section>

    <!-- thumbnails -->
    <div class="thumbnails">
      <ul>
        <li class="mr-3"><figure class="first"></figure></li>
        <li class="mr-3"><figure class="active second"></figure></li>
        <li><figure class="third"></figure></li>
      </ul>
    </div>

    <!-- hero subtitle -->
    <div class="hero-subtitle">
      <h6 class="f-xs f-sectra">Photographer</h6>
    </div>
    <!-- hero img -->
    <div class="hero-img"></div>
    <!-- hero patterns -->
    <img class="fade-in pattern-01" src="../assets/img/01-waves.svg" alt="">
    <img class="fade-in pattern-02" src="../assets/img/02-waves.svg" alt="">
    <!-- hero title -->
    <div class="hero-title">
      <h1 class="f-xxl f-graphik bold">
        <span class="op-0">Susan</span>
        <span class="op-0">Stripling</span>
      </h1>
    </div>
    <!-- year subtitle -->
    <div class="year-subtitle">
      <h6 class="f-sm f-sectra">—2018</h6>
    </div>

  </div>
</template>


<!-- style -->
<style lang="scss" scoped>
  @import '../assets/style/grid.scss';

  .bg {
    position: relative;
    width: 100vw; height: 100vh;
    max-height: 1300px;
    background: #e3ecff;
    overflow: hidden;
  }

  section {
    position: relative;
    height: 100vh;
  }

  .intro {
    width: grid-width(7);
    margin-top: 18rem;
  }

  .question-link {
    position: relative;
    z-index: var(--z1);
    cursor: pointer;

    width: 24%;

    transition: all 400ms ease;
    will-change: transform;
  }

  .question-link:after {
    content: '';
    // background: var(--sagan);
    background: rgba(181,196,230,1);
    display: block;
    position: relative;
    z-index: var(--zmin);
    width: 72%;
    height: 24px;
    transform: translate(56px,0);
    transition: all 400ms ease;
    will-change: transform;
    margin-top: -23px;
  }

  .question-link:hover { color: #0633FF; transform: translateX(10px); }
  .question-link:hover:after { transform: translateX(32px) scale(0.8,1); }

  .thumbnails {
    position: absolute;
    bottom: 2rem; left: 50%;
    max-width: var(--max_width);
    width: 92vw;
    transform: translateX(-50%);
  }

  .hero-subtitle {
    position: absolute;
    bottom: 384px; right: 504px;
  }

  .hero-img {
    position: absolute;
    bottom: 0px; right: 96px;
    z-index: var(--z2);

    width: 600px; height: 740px;
    transform: translateX(70px) scale(.9);
    transform-origin: bottom;

    background: url('../assets/img/0202-lg.png') no-repeat center center;
    background-size: cover;
  }

  .hero-title {
    position: absolute;
    bottom: 9.6rem; right: 59rem;
    z-index: var(--z1);

    color: #b4c4e8;

    span { display: block; }
    span:nth-of-type(1) { animation: spanOne 1400ms ease 700ms forwards; }
    span:nth-of-type(2) { animation: spanTwo 1400ms ease 800ms forwards; transform: translateX(5.6rem); }
  }

  .pattern-01 {
    position: absolute;
    bottom: 160px; right: 432px;
    z-index: var(--z1);

    // animation: fadeIn 300ms ease 300ms forwards;
  }

  .pattern-02 {
    position: absolute;
    bottom: 280px; right: 96px;
    z-index: var(--z1);

    // animation: fadeIn 300ms ease 350ms forwards;
  }

  .year-subtitle {
    position: absolute;
    bottom: 50%; right: 32px;
    transform: translateY(-50%) rotate(90deg);
  }

  figure {
    width: 64px; height: 64px;
    border-radius: 4px;
    border: 2px solid #fff;
    background: #fff7ff;
    background-size: cover;

    cursor: pointer;
    transition: var(--ease);

    &:hover { box-shadow: 0 8px 20px 0 #A6B7DF; transform: translateY(-8px); }
  }

  figure.first {
    background: url('../assets/img/01-thumb.png') no-repeat center center;
    background-size: cover;
  }

  figure.second {
    background: url('../assets/img/02-thumb.png') no-repeat center center;
    background-size: cover;
  }

  figure.third {
    background: url('../assets/img/03-thumb.png') no-repeat center center;
    background-size: cover;
  }

  figure.active { box-shadow: 0 8px 20px 0 #A6B7DF; transform: translateY(-8px) scale(1.1); }

  // anim
  @keyframes spanOne {
    from { opacity: 0; transform: translateX(-4rem); }
    to   { opacity: 1; transform: translateX(0); }
  }

  @keyframes spanTwo {
    from { opacity: 0; transform: translateX(9.6rem); }
    to   { opacity: 1; transform: translateX(5.6rem); }
  }

</style>


<!-- logic -->
<script>
  export default { name: 'heroTwo' }
</script>
