<template>
  <div>
    <seo
      title='Hakkımızda | Şanlı Medikal',
      description='Firmamız 1985 yılında Urfa Medikal adı altında bölgede ilk medikal sektöründe faaliyete girmiş olup 1992 yılında Şanlı Medikal olarak isim değişikliği yaparak yoluna devam etmiştir.'
    />
    <About />
    <bayiler />
  </div>
</template>

<script>
import About from "~/components/about"
import seo from '~/components/seo'
import bayiler from '~/components/bayiler'
export default {
  name: 'hakkimizda',
  components:{
    About,
    seo,
    bayiler
  },
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 1000)
    })
  }
}
</script>

<style scoped>

</style>
