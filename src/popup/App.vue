<template>
  <v-app>
    <v-toolbar app flat dark>
      <v-toolbar-items>
        <v-btn flat to="/" style="margin-left: -1.15rem;border-radius: 0">Platines</v-btn>
        <v-btn flat to="/playlist" style="border-radius: 0">Play List</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-content><router-view></router-view></v-content>
  </v-app>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style lang="sass"></style>
