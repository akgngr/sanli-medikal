<template>
<b-container>
  <b-row>
    <b-col lg='6' sm='12'>
      <b-img-lazy class='catalog-img lazyload' v-bind="mainProps" data-src="/images/scientist-working-at-lab.jpg" alt="IŞanlı Medikal Katalog" />
    </b-col>
    <b-col lg='6' sm='12' class='d-flex justify-content-center align-items-start flex-column'>
      <h2>Ürün Kataloglarımız</h2>
      <p>Ürün kataloglarımızı iceleyerek hangi ürünlerin bayiisi olduğumuzu görebilir ve bizden ilgili ürün hakkında teklif isteyebilirsiniz.</p>
      <nuxt-link to='/urunler' class='btn btn-outline-primary btn-lg'>Ürün Katalogları</nuxt-link>
    </b-col>
  </b-row>
</b-container>
</template>

<script>
export default {
  name: 'catalog',
  data() {
    return {
      mainProps: {
        center: true,
        fluidGrow: true,
        blank: true,
        blankColor: '#bbb',
        width: 400,
        height: 200,
        class: 'my-5'
      }
    }
  }
}
</script>

<style scoped>

</style>
