<template>
  <header>
    <b-navbar toggleable="lg" type="dark" variant="secondary" sticky>
      <b-navbar-brand href="#">
        <img width='55%' src='/trans_logo.svg' alt='Şanlı Medkial'>
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="/">Anasayfa</b-nav-item>
          <b-nav-item href="#">Hakkımızda</b-nav-item>
          <b-nav-item href="#">Ürünlerimiz</b-nav-item>
          <b-nav-item href="#">İletişim</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </header>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style scoped>

</style>
