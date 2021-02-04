<template>
  <div>
    <seo
      title='Şanlı Medikal'
      description='Firmamız 1985 yılında Urfa Medikal adı altında bölgede ilk medikal sektöründe faaliyete girmiş olup 1992 yılında Şanlı Medikal olarak isim değişikliği yaparak yoluna devam etmiştir.'
    />
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
import seo from '~/components/seo'

export default {
  layout: 'default',
  components: {
    Slideshow,
    About,
    Bayiler,
    Catalog,
    Contact,
    Bilgilendirme,
    seo
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
