<template>
<div>
  <seo
    title='İletişim | Şanlı Medikal'
    description='Bizimle iletişime geçin. Şanlı Medikal.'
  />
  <b-container class='pt-5 pb-5 mt-5 mb-5' fluid='xl'>
    <b-row>
      <b-col>
        <h1 class='pt-3 pb-5'>Bizimle İletişime Geçin</h1>
        <p><span><b>Adres:</b><a class='text-secondary' target='_blank' href='https://goo.gl/maps/NoZtN9mcZgDmXVJy7'> Akpıyar Mah. 4051 Sok. No 14/C/B Karaköprü/Şanlıurfa</a></span></p>
        <p>
          <span><b>Telefon:</b> <a class='text-secondary' href='tel:+904143133879'>0(414) 313 3879</a></span>
        </p>
        <p>
          <span><b>Fax:</b> <a class='text-secondary' href='tel:+904143124438'>0(414) 312 4438</a></span>
        </p>
        <p>
          <span><b>Eposta:</b> <a class='text-secondary' href='mailto:sanlimedikal@sanlimedikal.com.tr'>sanlimedikal@sanlimedikal.com.tr</a></span>
        </p>
        <p>
          <span><b>Eposta 2:</b> <a class='text-secondary' href='mailto:infosanlimedikal@gmail.com'>infosanlimedikal@gmail.com</a></span>
        </p>
      </b-col>
      <b-col>
        <h2 class='pt-2 pb-3'>İletişim Formu</h2>
        <b-form
          method="POST"
          name='ContctForm'
          data-netlify="true"
          data-netlify-honeypot="bot-field"
        >
          <b-form-group
            id="input-group-1"
            label="Eposta adresi:"
            label-for="input-1"
          >
            <b-form-input
              id="input-1"
              name="email"
              type="email"
              placeholder="Eposta adresinizi giriniz."
              required
            ></b-form-input>
          </b-form-group>

          <b-form-group
            id="input-group-1"
            label="Telefon Numaranız:"
            label-for="input-1"
          >
            <b-form-input
              id="input-1"
              name="phone"
              type="text"
              placeholder="Telefon numaranızı giriniz"
              required
            ></b-form-input>
          </b-form-group>

          <b-form-group id="input-group-2" label="Adınız, soyadınız:" label-for="input-2">
            <b-form-input
              id="input-2"
              name="name"
              placeholder="Adınız ve soyadınızı girin"
              required
            ></b-form-input>
          </b-form-group>

          <b-form-group
            id="textarea-1"
            label="Mesajınız:"
            label-for="textarea"
          >
            <b-form-textarea
              id="textarea"
              name="message"
              placeholder="Mesajınızı yazınız..."
              rows="3"
              max-rows="6"
            ></b-form-textarea>
          </b-form-group>

          <b-button type="submit" variant="outline-primary">Gönder</b-button>
        </b-form>
      </b-col>
    </b-row>
  </b-container>
  <b-row>
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3179.082969501278!2d38.8060259500836!3d37.174499159956135!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1534703a60f4c40f%3A0xec529a9b8a747972!2zT3NtYW4gR2F6aSwgMzk3LiBTay4gTm86MTcsIDYzMzAwIMWeYW5sxLF1cmZhIE1lcmtlei_FnmFubMSxdXJmYQ!5e0!3m2!1str!2str!4v1612339439038!5m2!1str!2str"
      width="100%"
      height="480"
      frameborder="0"
      style="border:0;"
      allowfullscreen=""
      aria-hidden="false"
      tabindex="0"></iframe>
  </b-row>
</div>
</template>

<script>
import seo from '~/components/seo'
import axios from 'axios'

export default {
  name: 'iletisim',
  components: {
    seo
  },
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 1000)
    })
  },
  methods: {
    encode (data) {
      return Object.keys(data)
        .map(
          key => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`
        )
        .join("&");
    },
    handleSubmit () {
      const axiosConfig = {
        header: { "Content-Type": "application/x-www-form-urlencoded" }
      };
      axios.post(
        "/",
        this.encode({
          "form-name": "ContctForm",
          ...this.form
        }),
        axiosConfig
      );
    }
  }
}
</script>

<style scoped>

</style>
