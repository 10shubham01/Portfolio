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
<style lang="scss" scoped>
#app {
  font-family: "Josefin Slab", serif;
  background: #fcfcfc;
  color: #000000;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  overflow: hidden;
  @media (max-width: 768px) {
    font-weight: bold !important;
  }
}
</style>
