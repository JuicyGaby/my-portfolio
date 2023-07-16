<template lang="">
  <div class="div-container d-flex flex-column">
    <Navbar ></Navbar>
    <v-container fluid class="about pa-0">
      <v-row class="about ma-0">
        <v-col class="d-flex flex-wrap jutsify-center mb-10 mb-sm-0" cols="12" md="6">
          <div class="details d-flex flex-fill justify-center align-center flex-column px-5">
            <p
            class="text-center text-lg-h2 text-md-h3 text-sm-h4 text-h3 font-weight-bold"
            :style="{ color: '#FF8303' }">Gabe Fletcher Sanchez</p>
            <p class="text-center text-h4 font-weight-medium" :style="{ color: '#F0E3CA' }">FullStack Developer</p>
            <p class="text-h6 text-center" :style="{ color: '#F0E3CA' }">Empowering Businesses through Seamless Digital Solutions.</p>
          </div>
        </v-col>
        <v-col class="d-flex justify-center align-center" cols="12" md="6">
          <v-sheet class="profile" width="25rem" height="25rem" height-sm="10rem" height-md="5rem" rounded="rounded" elevation="10"></v-sheet>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
import Navbar from '../components/Navbar.vue'
export default {
  components: {
    Navbar,
  }
}
</script>

<style lang="css" scoped>

div {
  /* border: var(--border); */
}
.about {
  height: 100%;
}
.details {
  gap: 1em;
}
.profile {
  background-image: url('/public/images/1.jpg');
  background-size: cover;
  background-position: top;
}
</style>