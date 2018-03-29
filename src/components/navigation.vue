<!-- layout -->
<template>
  <nav class="">

    <div class="wrapper mw__lg">
      <div class="nav__left">
        <svg width="40" height="32"><path d="M0 12.63V4.529C0 2.515 1.912 0 4.298 0h7.698L8.652 3.52H4.298c-.474 0-.954.501-.954 1.008v4.581L0 12.631zM11.996 32H4.298C2.388 32 0 29.986 0 27.47v-8.1l3.344 3.52v4.58c0 .507.48 1.01.954 1.01h4.355L11.996 32zm28.005-12.63v8.1c0 2.013-1.91 4.53-4.3 4.53h-7.695l3.342-3.52h4.353c.478 0 .954-.504.954-1.01v-4.58l3.346-3.52zM28.006 0h7.695c1.91 0 4.3 2.01 4.3 4.528v8.103L36.655 9.11V4.528c0-.507-.477-1.007-.955-1.007h-4.353L28.006 0z" fill="#0F2D36"/></svg>
      </div>
      <div class="nav__right">
        <ul class="f-sectra f-md bold">
          <li>Share</li>
          <li class="ml-9">Sell</li>
          <li class="ml-9">Grow</li>
          <li class="ml-0 f-sm bold f-graphik uc"><a class="ml-9 f-graphik uc" href="https://studio.shootproof.com/v2/login" data-title="Sign Up"></a></li>
        </ul>
      </div>
    </div>

  </nav>
</template>


<!-- style -->
<style scoped lang="scss">
  nav {
    position: fixed;
    z-index: var(--zmax);
    position: fixed;
    left: 50%;
    transform: translateX(-50%);
    width: 100%;

    padding: 3.2rem 0 1.2rem 0;

    transition: all 600ms ease;
    will-change: padding;
  }

  nav.fade-in {
    background: rgba(255,255,255,1);
    box-shadow: 0 1px 0 rgba(0,0,0,.1);
    padding: 1.2rem 0 1.2rem 0;
  }

  .wrapper {
    display: flex;
    width: 100%;
  }

  .nav__left { flex-grow: 1; margin-top: 6px; }
  .nav__right { margin-top: 1px; }

  a {
  	position: relative;
  	display: inline-block;
  	padding: 0.8em 2.4em;
  	text-decoration: none;
  	text-align: center;
  	cursor: pointer;
  	user-select: none;
  	color: white;

  	&::before {
  		content: '';
  		position: absolute;
  		top: 0;
  		left: 0;
  		bottom: 0;
  		right: 0;
      background-image: linear-gradient(45deg, #FC9495 0%, #0633FF 100%);
  		border-radius: 4px;
  		transition: box-shadow .5s ease, transform .2s ease;
  		will-change: transform;
  		box-shadow: 0 2px 5px rgba(26,36,145,0.2);
  		transform:
  			translateY(var(--ty, 0))
  			rotateX(var(--rx, 0))
  			rotateY(var(--ry, 0))
  			translateZ(var(--tz, -12px));
  	}

  	&:hover::before { box-shadow: 0 5px 15px rgba(26,36,145,0.3); }

  	&::after {
  		position: relative;
  		display: inline-block;
  		content: attr(data-title);
  		transition: transform .2s ease;
  		letter-spacing: .01em;
  		will-change: transform;
  		transform:
  			translateY(var(--ty, 0))
  			rotateX(var(--rx, 0))
  			rotateY(var(--ry, 0));
  	}
  }

</style>


<!-- logic -->
<script>
  export default {
    name: 'navigation',

    mounted() {
      let scrollpos = window.scrollY
      const header = document.querySelector("nav")
      const header_height = header.offsetHeight
      const add_class_on_scroll = () => header.classList.add("fade-in")
      const remove_class_on_scroll = () => header.classList.remove("fade-in")

      window.addEventListener('scroll', function() {
        scrollpos = window.scrollY;
        if (scrollpos >= header_height) { add_class_on_scroll() }
        else { remove_class_on_scroll() }
      });


      var docStyle = document.documentElement.style;
      var aElem = document.querySelector('a');
      var boundingClientRect = aElem.getBoundingClientRect();

      aElem.onmousemove = function (e) {

      	var x = e.clientX - boundingClientRect.left;
      	var y = e.clientY - boundingClientRect.top;

      	var xc = boundingClientRect.width / 2;
      	var yc = boundingClientRect.height / 2;

      	var dx = x - xc;
      	var dy = y - yc;

      	docStyle.setProperty('--rx', dy / -1 + 'deg');
      	docStyle.setProperty('--ry', dx / 10 + 'deg');
      };

      aElem.onmouseleave = function (e) {

      	docStyle.setProperty('--ty', '0');
      	docStyle.setProperty('--rx', '0');
      	docStyle.setProperty('--ry', '0');
      };

      aElem.onmousedown = function (e) {

      	docStyle.setProperty('--tz', '-25px');
      };

      document.body.onmouseup = function (e) {

      	docStyle.setProperty('--tz', '-12px');
      };
    }
  }
</script>
