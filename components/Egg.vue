<template>
  <div>
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

  .main-egg {
    margin-top: 600px;
    width: 154px;
    height: 186px;
    position: relative;
    background: radial-gradient(ellipse at 40px 30px, $eggColor2 20%, $eggColor 40%);
    border-radius: 50% 50% 48% 48%/ 58% 58% 42% 42%;
    overflow: hidden;
    animation:
      eggShake 1.5s ease 0s 2 alternate forwards,
      eggShake2 1s ease 3s alternate forwards,
      eggOpen 1.5s ease 4s alternate forwards;
    transform-origin: bottom center;
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
      transform: translate(0,0);
    }
    100% {
      transform: translate(0,-100px);
    }
  }
  @keyframes eggOpen {
    0% {
      opacity: 1;
    }
    100% {
      opacity: 0;
    }
  }
</style>
