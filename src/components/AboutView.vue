<template lang="">
  <div class="div-container d-flex flex-column">
    <Navbar ></Navbar>
    <v-container fluid class="about pa-0">
      <v-row class="border-red ma-0">
        <v-col class="d-flex flex-wrap jutsify-center">
          <div class="details d-flex flex-fill justify-center align-center flex-column px-5">
            <p
            class="text-center text-lg-h2 text-md-h3 text-sm-h4 text-h3 font-weight-bold"
            :style="{ color: '#FF8303' }">Gabe Fletcher Sanchez</p>
            <p class="text-center text-h4 font-weight-medium" :style="{ color: '#F0E3CA' }">FullStack Developer</p>
            <p class="text-h6 text-center" :style="{ color: '#F0E3CA' }">Empowering Businesses through Seamless Digital Solutions.</p>
          </div>
        </v-col>
        <v-col class="d-flex justify-center align-center">
            <img src="http://placehold.it/360x400" alt="Dummy Image" />
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
.border-red {
  height: 100%;
}
div {
  border: var(--border);
}
.about {
  height: 100%;
}
.details {
  gap: 1em;
}
</style>