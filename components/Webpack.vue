<template>
  <div class="wrap">
    <div class="webpack">
      <div class="webpack_trapezoid webpack_trapezoid01"></div>
      <div class="webpack_trapezoid webpack_trapezoid02"></div>
      <div class="webpack_trapezoid webpack_trapezoid03"></div>
      <div class="webpack_trapezoid webpack_trapezoid04"></div>
      <div class="webpack_trapezoid webpack_trapezoid05"></div>
      <div class="webpack_trapezoid webpack_trapezoid06"></div>
      <div class="webpack_center">
        <div class="webpack_rhombus webpack_rhombus01"></div>
        <div class="webpack_rhombus webpack_rhombus02"></div>
        <div class="webpack_rhombus webpack_rhombus03"></div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Webpack"
  }
</script>

<style scoped lang="scss">
  .wrap {
    height: 100%;
    align-items: center;
    display: flex;
    margin-top: 120px;
  }
  .webpack {
    margin: auto;
    width: 400px;
    position: relative;
  }
  .webpack_rhombus {
    width: 105px;
    height: 93px;
    background-color: #1c78c0;
    position: absolute;
  }
  .webpack_rhombus01 {
    transform: rotate(-30deg) skew(30deg);
    top: 0;
    right: 0;
    left: 0;
    margin: auto;
  }
  .webpack_rhombus02 {
    transform: rotate(30deg) skew(30deg);
    left: -11px;
    top: 92px;
  }
  .webpack_rhombus03 {
    transform: rotate(-90deg) skew(30deg);
    top: 92px;
    right: -11px;
  }

  .webpack_center {
    position: relative;
    width: 190px;
    height: 210px;
    margin: auto;
  }
  .webpack_trapezoid {
    width: 183px;
    height: 60px;
    position: absolute;
    &::before,&::after {
      position: absolute;
      top: 0;
      width: 50%;
      height: 100%;
      content: '';
      background-color: #8ed5fa;
    }
    &::before {
      left: 0;
      transform: skewX(-30deg);
      transform-origin: 0 100%;
    }
    &::after {
      right: 0;
      transform: skewX(30deg);
      transform-origin: 100% 100%;
    }
  }
  .webpack_trapezoid01 {
    transform: rotate(150deg);
    top: -49px;
    left: 36px;
  }
  .webpack_trapezoid02 {
    transform: rotate(90deg);
    top: 77px;
    left: -36px;
  }
  .webpack_trapezoid03 {
    transform: rotate(30deg);
    top: 204px;
    left: 35px;
  }
  .webpack_trapezoid04 {
    transform: rotate(-150deg);
    top: -49px;
    right: 36px;
  }

  .webpack_trapezoid05 {
    transform: rotate(-90deg);
    top: 77px;
    right: -36px;
  }

  .webpack_trapezoid06 {
    transform: rotate(-30deg);
    top: 204px;
    right: 35px;
  }
</style>
