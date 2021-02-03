<template>
<b-row>
  <b-col>
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3179.082969501278!2d38.8060259500836!3d37.174499159956135!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1534703a60f4c40f%3A0xec529a9b8a747972!2zT3NtYW4gR2F6aSwgMzk3LiBTay4gTm86MTcsIDYzMzAwIMWeYW5sxLF1cmZhIE1lcmtlei_FnmFubMSxdXJmYQ!5e0!3m2!1str!2str!4v1612339439038!5m2!1str!2str"
      width="100%"
      height="480"
      frameborder="0"
      style="border:0;"
      allowfullscreen=""
      aria-hidden="false"
      tabindex="0"></iframe>
  </b-col>
  <b-col>
    <b-form
      name='ContctForm'
      data-netlify="true"
      data-netlify-honeypot="bot-field"
    >
      <input type="hidden" name="form-name" value="contact">
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

      <b-button type="submit" variant="primary">Submit</b-button>
    </b-form>
  </b-col>
</b-row>
</template>

<script>
export default {
  name: 'contact'
}
</script>

<style scoped>

</style>
