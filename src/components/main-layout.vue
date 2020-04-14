<template>
  <v-app class="app">
    <AppBar />
    <Navigation />
    <v-content class="content">
      <router-view />
    </v-content>
  </v-app>
</template>

<style lang="scss" scoped>
.app {
  height: 100vh;
}

.content {
  height: 100%;
  margin: 0.5em;

  .v-content__wrap {
    overflow: auto;
    padding-bottom: 20px;
    padding-top: 20px;
  }
}
</style>

<script>
import AppBar from './app-bar.vue';
import Navigation from './navigation-drawer.vue';
export default {
  name: 'Layout',
  components: {
    AppBar,
    Navigation,
  },
};
</script>
