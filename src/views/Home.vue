<!-- layout -->
<template>
  <div>
    <div class="hero">
      <section class="mw__lg debug">

        <div class="intro">
          <!-- headline -->
          <h1 class="mb-4 measure-6 f-xl f-sectra bold">See how ShootProof Galleries can make photograpy better and brighter.</h1>
          <!-- intro copy -->
          <p class="mb-6 f-graphik">Galleries are a single space for creating and sharing together. Work seamlessly with all types of photos—from weddings and portrait, to seniors and newborns.</p>
          <!-- button -->
          <div class="question-link">
            <a class="transition">
              <h4 class="f-sm f-graphik bold">See Susan's Gallery</h4>
            </a>
          </div>

          <!-- thumbnails -->
          <div class="thumbnails">
            <ul>
              <li class="mr-3">
                <figure class="active first"></figure>
              </li>
              <li class="mr-3">
                <figure class="second"></figure>
              </li>
              <li>
                <figure class="third"></figure>
              </li>
            </ul>
          </div>
        </div>

      </section>
    </div>
  </div>
</template>


<!-- style -->
<style lang="scss" scoped>

  .hero {
    position: absolute;
    top: 0; left: 0;
    z-index: var(--zmin);

    width: 100vw; height: 100vh;
    background: #eaecf9;
  }

  .intro {
    position: relative;
    padding: 20rem 0;
    height: 96vh;

    p { max-width: 36%; }

    .question-link {
      position: relative;
      z-index: var(--z1);
      cursor: pointer;

      width: 14%;

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
      bottom: 0;
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
  }

</style>


<!-- logic -->
<script>
  export default { name: 'home' }
</script>
