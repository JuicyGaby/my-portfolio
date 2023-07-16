<template lang="">
  <div class="div-container" id="skills">
    <v-container class="skills d-flex flex-column justify-center align-center">
      <p class="text-h3 font-weight-bold mb-5" :style="{ color: '#FF8303' }">Technologies</p>
      <div class="d-flex flex-column justify-center align-center">
        <v-row class=" ma-0">
          <v-col v-for="tech in isLanguage">
            <p class="text-h2 text-sm-h1 d-flex justify-center">
              <v-icon :color="tech.color" :icon="getIcon(tech)"></v-icon>
            </p>
          </v-col>
        </v-row>
        <v-row class=" ma-0">
          <v-col v-for="tech in notALanguage">
            <p class="text-h2 text-sm-h1 d-flex justify-center ">
              <v-icon :color="tech.color" :icon="getIcon(tech)"></v-icon>
            </p>
          </v-col>
        </v-row>
      </div>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      technologies: [
        { isLanguage: true, name: 'html5', color: 'orange-darken-4' },
        { isLanguage: true, name: 'css3', color: 'blue-darken-4' },
        { isLanguage: true, name: 'javascript', color: 'yellow-darken-3' },
        { isLanguage: true, name: 'python', color: 'indigo-darken-3' },
        { isLanguage: false, name: 'nodejs', color: 'green-darken-4' },
        { isLanguage: false, name: 'vuejs', color: 'light-green-darken-4' },
        { isLanguage: false, name: 'react', color: 'blue-darken-2' },
        { isLanguage: false, name: 'git', color: 'orange-darken-4' },
      ],
    }
  },
  computed: {
    isLanguage() {
      return this.technologies.filter(item => item.isLanguage)
    },
    notALanguage() {
      return this.technologies.filter(item => !item.isLanguage)
    }
  },
  methods: {
    getIcon(tech) {
      if (tech.isLanguage) return `mdi-language-${tech.name}`
      return `mdi-${tech.name}`
    },
  },
}
</script>
<style lang="css" scoped>
div {
  border: var(--border)
}

.grid-col {
  display: flex;
  align-items: center;
  justify-content: center;
}

.skills {
  height: 100%;
}
</style>