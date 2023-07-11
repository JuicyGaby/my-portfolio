<template lang="">
  <div class="">
    <AboutView ></AboutView>
    <Skills ></Skills>
  </div>
  <!-- <Skills ></Skills> -->
</template>
<script>
import AboutView from '../components/AboutView.vue';
import Skills from '../components/SkillsView.vue'
import Projects from '../components/ProjectsView.vue'
import Footer from '../components/Footer.vue'

export default {
  components: {
    AboutView,
    Skills
  },
  data() {
    return {
      
    }
  },
}
</script>
<style lang="css" scoped>
.div-container{
  height: 100vh;
  width: 100%;
  background-color: var(--darkBG);
}
</style>