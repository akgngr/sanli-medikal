<template>
<About />
</template>

<script>
import About from "~/components/about"
export default {
  name: 'hakkimizda',
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
