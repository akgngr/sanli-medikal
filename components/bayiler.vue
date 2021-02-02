
<template>
  <div>
    <vue-horizontal-list :items="items" :options="options">
      <template v-slot:default="{ item }">
        <div class="item">
          <p v-html='item.content'></p>
        </div>
      </template>
    </vue-horizontal-list>
  </div>
</template>

<script>
import VueHorizontalList from "vue-horizontal-list"

export default {
  name: "responsive",
  components: {
    VueHorizontalList,
  },
  data() {
    return {
      items: [
        '/images/bayiler/biorad.gif',
        '/images/bayiler/ClaimRechts.png',
        '/images/bayiler/megazol.png',
        '/images/bayiler/nonin.png',
        '/images/bayiler/okuman.png',
        '/images/bayiler/thermofisher.webp',
        '/images/bayiler/werfen.png'
      ].map((i) => {
        return {
          content: `<img class='image' src='${i}'>`,
        };
      }),
      options: {
        responsive: [
          { end: 576, size: 1 },
          { start: 576, end: 768, size: 2 },
          { start: 768, end: 992, size: 3 },
          { size: 4 },
        ],
      autoplay: {
        play: true,
        speed: 2800,
        repeat: true,
      }
      },
    };
  },
};
</script>

<style>
.item {
  padding: 24px;
}
.image{
  width: 100%;
}
</style>
