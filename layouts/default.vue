<template>
  <v-app>
    <v-main :class="theme ? 'dark' : 'light'">
      <Header @theme="switchThetheme($event)" />
      <Loading v-if="loading" />
      <Nuxt v-else />
    </v-main>
  </v-app>
</template>

<script>
import Header from "../components/header.vue";
import Loading from "../components/loading.vue";
export default {
  name: "DefaultLayout",
  component: {
    Header,
    Loading,
  },
  data() {
    return {
      theme: false,
      loading: true,
    };
  },
  mounted() {
    this.onLoading();
  },
  methods: {
    switchThetheme(theme) {
      this.theme = theme;
    },
    onLoading() {
      setTimeout(() => {
        this.loading = false;
      }, 3000);
    },
  },
};
</script>
<style lang="scss" scoped>
#app {
  font-family: "Josefin Slab", serif;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  overflow: hidden;
  @media (max-width: 768px) {
    font-weight: bold !important;
  }
  .dark {
    background-color: #222222 !important;
    color: #ffffff !important;
    transition-delay: 0.3s;
  }
  .light {
    background-color: #fcfcfc;
    color: #000000;
    transition-delay: 0.3s;
  }
}
</style>
