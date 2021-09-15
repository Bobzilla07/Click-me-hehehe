
<html>
  <head>
          <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Black+Ops+One&effect=fire|neon|outline|emboss|shadow-multiple|anaglyph|brick-sign|canvas-print|crackle|decaying">
      <style>
          @mixin sp-layout {
  @media screen and (max-width: 750px) {
    @content;
  }
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
   background: radial-gradient(ellipse at bottom, #0d1d31 0%, #0c0d13 100%);
  overflow: hidden;
}

@function random_range($min, $max) {
  $rand: random();
  $random_range: $min + floor($rand * (($max - $min) + 1));
  @return $random_range;
}

.stars {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 120%;
  transform: rotate(-45deg);
}

.star {
  $star-count: 50;
  --star-color: var(--primary-color);
  --star-tail-length: 6em;
  --star-tail-height: 2px;
  --star-width: calc(var(--star-tail-length) / 6);
  --fall-duration: 9s;
  --tail-fade-duration: var(--fall-duration);

  position: absolute;
  top: var(--top-offset);
  left: 0;
  width: var(--star-tail-length);
  height: var(--star-tail-height);
  color: var(--star-color);
  background: linear-gradient(45deg, currentColor, transparent);
  border-radius: 50%;
  filter: drop-shadow(0 0 6px currentColor);
  transform: translate3d(104em, 0, 0);
  animation: fall var(--fall-duration) var(--fall-delay) linear infinite, tail-fade var(--tail-fade-duration) var(--fall-delay) ease-out infinite;
  
  @include sp-layout {
    // For mobile performance, tail-fade animation will be removed QAQ
    animation: fall var(--fall-duration) var(--fall-delay) linear infinite;
  }

  @for $i from 1 through $star-count {
    &:nth-child(#{$i}) {
      --star-tail-length: #{random_range(500em, 750em) / 100};
      --top-offset: #{random_range(0vh, 10000vh) / 100};
      --fall-duration: #{random_range(6000, 12000s) / 1000};
      --fall-delay: #{random_range(0, 10000s) / 1000};
    }
  }

  &::before, &::after {
    position: absolute;
    content: '';
    top: 0;
    left: calc(var(--star-width) / -2);
    width: var(--star-width);
    height: 100%;
    background: linear-gradient(45deg, transparent, currentColor, transparent);
    border-radius: inherit;
    animation: blink 2s linear infinite;
  }

  &::before {
    transform: rotate(45deg);
  }

  &::after {
    transform: rotate(-45deg);
  }
}

@keyframes fall {
  to {
    transform: translate3d(-30em, 0, 0);
  }
}

@keyframes tail-fade {
  0%, 50% {
    width: var(--star-tail-length);
    opacity: 1;
  }

  70%, 80% {
    width: 0;
    opacity: 0.4;
  }

  100% {
    width: 0;
    opacity: 0;
  }
}

@keyframes blink {
  50% {
    opacity: 0.6;
  }
}
          
  h1 {
    color: #000000;
    text-shadow: 1px 1px 2px #00ff00, 0 0 25px #000000, 0 0 5px #00ff00;
  }
     h2 {
    color: #00ff;
    text-shadow: 1px 1px 2px #00ff, 0 0 25px #000000, 0 0 5px #00ff;
  }
body {
  font-family: "Black Ops One", sans-serif;
  font-size: 10px;
}
  
    
  </style>
    <meta charset="UTF-8">
    <script src="script.js"></script>
    <!-- <link rel="stylesheet" type="text/css" href="styles.css"> -->
  </head>
  <body>
      <div class="stars">
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
  <div class="star"></div>
</div>
    <h1>Welcome!</h1> 
    <h2>Clickers</h2>
    
      <select id="select" onchange="
var win = window.open(this.value, '_blank');
  win.focus();
">
<option value="">Clickers</option>
<option value="https://codepen.io/bobzilla07-the-animator/pen/rNMyjxw">Bobzilla07s Cookie Clicker</option>
<option value="https://codepen.io/bobzilla07-the-animator/pen/dypVyBd">Dylans Donut Clciker</option>
<option value="https://trixter9994.github.io/Cookie-Clicker-Source-Code/">Trixter9994 Cookie Clicker</option>

    </select>

    <h2>Pokemon</h2>
  <select id="select" onchange="
var win = window.open(this.value, '_blank');
  win.focus();
">
<option value="">Ouroborzo Pokemon</option>
<option value="http://ouroboroz.github.io/gba/launcher.html#pokemonlightplat">Pokemon Light Platnium</option>
<option value="http://ouroboroz.github.io/gba/launcher.html#pokemondarkviolet">Pokemon Dark Violet</option>
<option value="http://ouroboroz.github.io/gba/launcher.html#pokemonglaze">Pokemon Glaze</option>
<option value="http://ouroboroz.github.io/gba/launcher.html#pokemonemerald">Pokemon Emerald</option>
<option value="http://ouroboroz.github.io/gba/launcher.html#pokemongreen">Pokemon Green</option>
<option value="http://ouroboroz.github.io/gba/launcher.html#pokemonred">Pokemon Red</option>
    </select>
      
      <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Black+Ops+One&effect=fire|neon|outline|emboss|shadow-multiple">
body {
  font-family: "Black Ops One", sans-serif;
  font-size: 10px;
}


      <p class="font-effect-neon">Sofia on Fire</p>
<p class="font-effect-outline">Lorem ipsum dolor sit amet.</p>
<p class="font-effect-fire">123456790</p>







