<template lang="">
  <div class="footer" id="contacts">
    <v-container class="pa-0 contacts">
      <v-row class="contacts ma-0">
        <v-col class="d-flex flex-column justify-center align-center pa-0" align-self="center">
          <div class="d-flex">
            <div class="" v-for="icon in icons">
              <v-btn size="x-large" color="#FF8303" :icon="getIcon(icon.name)" variant="text"></v-btn>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      icons: [
        {name: 'facebook'},
        {name: 'linkedin'},
        {name: 'github'},
        {name: 'instagram'},
      ]
    }
  },
  methods: {
    getIcon(name) {
      return `mdi-${name}`
    }
  },
}
</script>
<style lang="css" scoped>
  div {
    /* border: var(--border); */
  }
  .footer {
    width: 100%;
    background-color: var(--darkBG);
  }
  .contacts {
    height: 100%;
  }
</style>