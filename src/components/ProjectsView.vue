<template lang="">
  <!-- <p class="text-h3 font-weight-bold" :style="{ color: '#FF8303' }">Projects</p> -->
  <div class="div-container" id="projects">
    <v-container  class="b2 projects">
      <v-row class="projects ma-0">
        <v-col align-self="center">
          <div class="d-flex justify-center align-center mb-5">
            <p class="text-h3 font-weight-bold" :style="{ color: '#FF8303' }">Projects</p>
          </div>
          <v-carousel cycle :show-arrows="false" color="#FF8303">
            <v-carousel-item
              src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
              cover
            ></v-carousel-item>

            <v-carousel-item
              src="https://cdn.vuetifyjs.com/images/cards/hotel.jpg"
              cover
            ></v-carousel-item>

            <v-carousel-item
              src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
              cover
            ></v-carousel-item>
          </v-carousel>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {

}
</script>
<style lang="css" scoped>
.projects {
  height: 100%;
}

div {
  /* border: var(--border); */
}

.b2 {
  /* border: var(--border2); */
}
</style>