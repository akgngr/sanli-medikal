<template>
  <div>
    <Slideshow />
    <About />
    <Bilgilendirme />
    <Catalog />
    <Bayiler />
    <Contact />
  </div>
</template>

<script>
import Slideshow from "/components/slideshow"
import About from "/components/about"
import Bayiler from "~/components/bayiler"
import Catalog from "~/components/catalog"
import Contact from "~/components/contact"
import Bilgilendirme from "~/components/bilgilendirme"

export default {
  layout: 'default',
  components: {
    Slideshow,
    About,
    Bayiler,
    Catalog,
    Contact,
    Bilgilendirme
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
