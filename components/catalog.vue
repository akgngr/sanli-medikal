<template>
<b-container>
  <b-row>
    <b-col lg='6' sm='12'>
      <b-img-lazy class='catalog-img' v-bind="mainProps" src="/images/scientist-working-at-lab.jpg" alt="IŞanlı Medikal Katalog" />
    </b-col>
    <b-col lg='6' sm='12' class='d-flex justify-content-center align-items-start flex-column'>
      <h2>Ürün Kataloglarımız</h2>
      <p>Ürün kataloglarımızı iceleyerek hangi ürünlerin bayiisi olduğumuzu görebilir ve bizden ilgili ürün hakkında teklif isteyebilirsiniz.</p>
      <b-button class='btn-lg' variant="outline-primary">Ürün Kataloğu İçin Tıklayın</b-button>
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
