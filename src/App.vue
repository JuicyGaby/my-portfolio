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
  --border2: 1px dashed blue;
  --darkBG: #1B1A17;
  --lightBG: #242320 ;
  --orangeDark: #A35709;
  --orangeLight: #FF8303;
  --textColor: #F0E3CA;
}

</style>
