
<template>
  <b-container class='pt-5 pb-5'>
    <vue-horizontal-list :items="items" :options="options">
      <template v-slot:default="{ item }">
        <div class="item">
          <span v-html='item.content'></span>
        </div>
      </template>
    </vue-horizontal-list>
  </b-container>
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
          { end: 576, size: 2 },
          { start: 576, end: 768, size: 3 },
          { start: 768, end: 992, size: 3 },
          { size: 5 },
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
