<template>
  <v-app class="main-page" dark>
    <v-toolbar flat height="50">
      <v-toolbar-items>
        <v-btn flat to="/" style="margin-left: -1.15rem;border-radius: 0">Platines</v-btn>
        <v-btn flat to="/playlist" style="border-radius: 0">Play List</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-content class="main-view"><router-view></router-view></v-content>
  </v-app>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style lang="sass">
.main-page
  height: 400px
  width: 600px
  .main-view
    height: calc(100% - 50px)
    overflow-y: auto
    overflow-x: hidden
</style>
