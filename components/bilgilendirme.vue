<template>
  <div class='bilgilendirme pb-5 mb-5 pt-5 mt-5'>
    <b-container>
      <b-row class='d-flex justify-content-center align-items-center'>
        <b-col lg='10'>Yılların vermiş olduğu tecrübemiz ile kurumunuzun labaratuvar hizmetlerini güvenceye alarak işinizi sağlama alın.</b-col>
        <b-col lg='2'>
          <router-link class='btn btn-outline-light btn-lg float-right' to='/iletisim'>İletişime Geç</router-link>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'bilgilendirme'
}
</script>

<style scoped>
.bilgilendirme{
  background: #37abed 51%;
  color: white;
  font-size: 18pt;
}
</style>
