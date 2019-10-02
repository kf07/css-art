<template>
  <section>
    <div>
<!--      <Egg />-->
      <Webpack />
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Egg from "../components/Egg";
import Webpack from "../components/Webpack";

export default {
  components: {
    Webpack,
    Egg,
    Logo
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
