<template>
  <div>
    <b-carousel
      id="carousel-fade"
      v-model="slide"
      :interval="4000"
      fade
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide img-src="/images/slide/akıllı-kalite-yonetimi.png" />

      <b-carousel-slide img-src="/images/slide/dl-kan-kultur-sistemleri.png" />

      <b-carousel-slide img-src="/images/slide/EURORealTime-SARS-CoV-2.png" />

      <b-carousel-slide img-src="/images/slide/indiko-plus-clinical-chemistry-analyzer.png" />

      <b-carousel-slide img-src="/images/slide/ULS-2100-floresan-immunoassay-analizor.png" />

      <b-carousel-slide img-src="/images/slide/IH-500-kan-bankasi-test-sistemi.png" />

      <b-carousel-slide img-src="/images/slide/Ih-1000-model-tam-otomatikimmunohemaotoloji-sistemleri.png" />
    </b-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null
    }
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true
    },
    onSlideEnd(slide) {
      this.sliding = false
    }
  }
}
</script>
