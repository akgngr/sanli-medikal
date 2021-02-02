<template>
  <div>
    <Slideshow />
    <div class="container">
      <About />
      <Bayiler />
      <Catalog />
    </div>
  </div>
</template>

<script>
import Slideshow from "/components/slideshow"
import About from "/components/about"
import Bayiler from "~/components/bayiler"
import Catalog from "~/components/catalog"

export default {
  layout: 'default',
  components: {
    Slideshow,
    About,
    Bayiler,
    Catalog
  },
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 500)
    })
  }
}
</script>

<style>

</style>
