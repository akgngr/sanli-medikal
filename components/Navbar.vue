<template>
    <b-navbar toggleable="lg" type="dark" variant="secondary" sticky>
      <b-navbar-brand href="/">
        <img width='55%' src='/trans_logo.svg' alt='Şanlı Medkial'>
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <nuxt-link class="nav-link" to="/" no-prefetch>Anasayfa</nuxt-link>
          <nuxt-link class="nav-link" to="/hakkimizda" no-prefetch>Hakkımızda</nuxt-link>
          <nuxt-link class="nav-link" to="/urunler" no-prefetch>Ürünlerimiz</nuxt-link>
          <nuxt-link class="nav-link" to="/iletisim" no-prefetch>İletişim</nuxt-link>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style scoped>
.nuxt-link-exact-active{
  color: #ffffff !important;
  font-width: 500;
}
</style>
