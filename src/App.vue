<template>
  <v-app>
    <v-main class="root">
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    //
  }),
}
</script>

<style lang="css" scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.root {
  --border: 1px dashed red;

}
.div-container {
  height: 100vh;
  width: 100%;
  border: var(--border);
}
</style>
