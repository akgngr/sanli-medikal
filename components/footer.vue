<template>
  <footer class='pt-5'>
    <b-container fluid='xl'>
      <b-row>
        <b-col lg='4' sm='12' class='pt-sm-0 '>
          <b-img-lazy class='footer-logo lazyload' data-src='/trans_logo.svg' />
        </b-col>
        <b-col lg='4' sm='12' class='pt-sm-0 pt-5 '>
          <p><span><b>Adres:</b><a target='_blank' href='https://goo.gl/maps/NoZtN9mcZgDmXVJy7'> Akpıyar Mah. 4051 Sok. No 14/C/B Karaköprü/Şanlıurfa</a></span></p>
          <p>
            <span><b>Telefon:</b> <a href='tel:+904143133879'>0(414) 313 3879</a></span>
          </p>
          <p>
            <span><b>Fax:</b> <a href='tel:+904143124438'>0(414) 312 4438</a></span>
          </p>
        </b-col>
        <b-col lg='4' sm='12' class='pt-sm-0 pt-5 '>
          <p>
            <span><b>Eposta:</b> <a href='mailto:sanlimedikal@sanlimedikal.com.tr'>sanlimedikal@sanlimedikal.com.tr</a></span>
          </p>
          <p>
            <span><b>Eposta 2:</b> <a href='mailto:infosanlimedikal@gmail.com'>infosanlimedikal@gmail.com</a></span>
          </p>
        </b-col>
      </b-row>
    </b-container>
    <span class='pb-5'></span>
    <hr />
    <b-container fluid class='pt-1 pb-3'>
      <small>Tüm hakları saklıdır. © Şanlı Medikal - {{ this.toyear }}, design by <a target='_blank' href="https://akgngr.github.com">akgngr</a> </small>
    </b-container>
  </footer>
</template>

<script>
const today = new Date();
const year = today.getFullYear();
export default {
  data() {
    return{
      toyear: year
    }
  }
}
</script>

<style scoped>
footer{
  background-color: var(--secondary);
  color: var(--light);
}
.footer-logo{
  width: 65%;
}
footer a{
  color: white;
}
</style>
