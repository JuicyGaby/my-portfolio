<template lang="">
  <div class="nav mb-10 mb-sm-0">
    <v-toolbar color="#1B1A17" elevation="5">
      <v-container fluid>
        <v-row>
          <v-col class="d-flex align-center">
            <a class="text-h5" href="https://github.com/JuicyGaby">
              <div class="d-flex align-center">
                <v-icon icon="mdi-github"></v-icon>
                <p class="font-weight-medium mx-2">JuicyGaby</p>
              </div>
            </a>
          </v-col> 
          <v-col class="hidden-sm-and-down">
            <div class="d-flex justify-space-between">
              <div v-for="link in navLinks">
                <a class="text-h6" :href="link.link" >{{link.tag}}</a>
              </div>
            </div>
          </v-col>
          <v-col class="hidden-md-and-up">
            <div class="d-flex justify-end">
              <p class="text-h5">
                  <v-icon :icon="drawerOpen ? 'mdi-menu-open' : 'mdi-menu'" color="#F0E3CA" @click="drawerOpen = !drawerOpen"></v-icon>
              </p>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-toolbar>
  </div>
</template>
<script>
export default {
  data() {
    return {
      drawerOpen: false,
      navLinks: [
        { tag: 'About Me', link: '#about'},
        { tag: 'Skills', link: '#skills'},
        { tag: 'Projects', link: '#projects'},
        { tag: 'Contacts', link: '#contacts'},
      ]
    }
  },
}
</script>
<style lang="css" scoped>
div {
  /* border: var(--border); */
}
a {
  text-decoration: none;
  color: var(--textColor);
  transition: all .3s;
}
a:hover {
  color: #FF8303;
}
</style>