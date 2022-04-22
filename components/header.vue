<template>
  <v-row>
    <v-col cols="12" class="d-flex justify-end pb-0 px-10">
      <v-switch
        width="100%"
        v-model="theme"
        color="orange darken-3"
        hide-details
        @change="switchTheme"
      ></v-switch>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data() {
    return {
      theme: false,
    };
  },
  methods: {
    switchTheme() {
      this.$emit("theme", this.theme);
    },
  },
};
</script>