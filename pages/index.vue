<template>
  <section>
    <div>
      <Egg />
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Egg from "../components/Egg";

export default {
  components: {
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
