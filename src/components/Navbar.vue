<template lang="">
  <div class="nav">
    <v-toolbar color="#1B1A17" elevation="5">
      <v-container fluid>
        <v-row>
          <v-col class="d-flex align-center">
            <p class="text-h6 text-white">JuicyGaby</p>
          </v-col> 
          <v-col class="hidden-sm-and-down">
            <div class="d-flex justify-space-between">
              <a class="text-h6" href="#skills">About Me</a>
              <a class="text-h6" href="#skills">Skills</a>
              <a class="text-h6" href="#skills">Projects</a>
              <a class="text-h6" href="#skills">Contacts</a>
            </div>
          </v-col>
          <v-col class="hidden-md-and-up">
            <div class="d-flex justify-end">
              <v-btn size="x-large" variant="plain">
                <v-icon :icon="drawerOpen ? 'mdi-menu-open' : 'mdi-menu'" color="#F0E3CA" @click="drawerOpen = !drawerOpen"></v-icon>
              </v-btn>
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
    }
  },
}
</script>
<style lang="css" scoped>
div {
  border: var(--border);
}
a {
  text-decoration: none;
  color: var(--textColor);
}
</style>