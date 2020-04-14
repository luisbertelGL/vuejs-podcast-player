<template>
  <v-app-bar app clipped-left>
    <router-link :to="{ name: 'home' }" class="link white--text">
      <v-img
        src="@/assets/app-bar-logo.png"
        contain
        alt="Gorilla logo"
        class="logo"
      />
      <v-toolbar-title class="title">Gorilla Cast</v-toolbar-title>
    </router-link>
  </v-app-bar>
  
</template>

<style lang="scss" scoped>
.logo {
  max-width: 40px;
}

.logo,
.title {
  display: inline-block;
  vertical-align: middle;
  margin-left: 0.5em;
}

.link {
  text-decoration: none;
  user-select: none;
}
</style>

<script>
export default {
  name: 'AppBar',
};
</script>
