<template>
  <v-app>
    <v-main>
      <Nuxt />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
};
</script>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Josefin+Slab:wght@300&family=Manrope:wght@300&display=swap");
#app {
  font-family: "Josefin Slab", serif;
  background: #fcfcfc;
  color: #000000;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  overflow: hidden;
}
</style>
