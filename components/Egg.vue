<template>
  <div class="back">
    <div class="shadow-light"></div>
    <div class="main-egg">
      <div class="pattern1 pattern"></div>
      <div class="pattern2 pattern"></div>
      <div class="pattern3 pattern"></div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Egg"
  }
</script>

<style scoped lang="scss">
  $eggColor: #f6f4c3;
  $eggColor2: #feffef;
  $patternColor1: #8ba566;
  $patternColor2: #9cb969;

  .back {
    background-color: #e2fae2;
    display: flex;
    justify-content: center;
    align-items: flex-end;
    height: 100vh;
    padding-bottom: 30px;
    overflow: hidden;
    position: relative;
  }
  .shadow-light {
    display: block;
    position: absolute;
    bottom: 180px;
    left: 0;
    right: 0;
    margin: auto;
    height: 100px;
    width: 100px;
    background-color: #fff;
    border-radius: 50%;
    box-shadow:12px 12px 6px 6px #ffffff;
    animation:
      eggOpen 2s ease 4s alternate forwards,
      eggOpen2 1.5s ease 5.3s alternate forwards;
    z-index: 3;
    transform: scale(0);
    transform-origin: center;
  }

  .main-egg {
    width: 154px;
    height: 186px;
    position: relative;
    background: radial-gradient(ellipse at 40px 30px, $eggColor2 20%, $eggColor 80%);
    border-radius: 50% 50% 48% 48%/ 58% 58% 42% 42%;
    overflow: hidden;
    animation: eggShake 1.5s ease 0s 2 alternate forwards,
    eggShake2 1s ease 3s alternate forwards;
    transform-origin: bottom center;
    box-shadow: 3px 6px 3px -2px gray;

    &::before {
      content: '';
      display: block;
      position: absolute;
      top: 0;
      left: 0;
      width: 0;
      height: 0;
      opacity: 0.75;
      filter: alpha(opacity=75);
      mix-blend-mode: overlay;
      border-radius: 50%;
      background-image: radial-gradient(ellipse at 0 0, $eggColor 30%, darken($eggColor,60%) 60%);
      z-index: 10;
    }
    > .pattern {
      background-color: $patternColor1;
      position: absolute;
    }

    > .pattern1 {
      width: 60px;
      height: 84px;
      top: 64px;
      left: 80px;
      transform: rotate(20deg);
      background: linear-gradient(to top, $patternColor1, 70%, lighten($patternColor1, 12%));;
      border-radius: 58% 42% 39% 61% / 54% 57% 43% 46%;
    }

    > .pattern2 {
      width: 33px;
      height: 33px;
      background-color: lighten($patternColor1, 15%);
      border-radius: 50%;
      right: 15px;
      top: 0;
    }

    > .pattern3 {
      width: 65px;
      height: 65px;
      border-radius: 50%;
      left: -32px;
      background-color: lighten($patternColor1, 15%);
    }
  }

  @keyframes eggShake {
    0% {
      transform: rotate(0deg);
    }
    25% {
      transform: rotate(25deg);
    }
    50% {
      transform: rotate(0deg);
    }
    75% {
      transform: rotate(-10deg);
    }
  }

  @keyframes eggShake2 {
    0% {
      transform: translate(0, 0);
    }
    100% {
      transform: translate(0, -100px);
    }
  }

  @keyframes eggOpen {
    0% {
      transform: scale(0);
    }
    100% {
      transform: scale(20);
    }
  }

  @keyframes eggOpen2 {
    0% {
      opacity: 1;
    }
    100% {
      opacity: 0;
    }
  }
</style>
