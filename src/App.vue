<template>
  <MainLayout />
</template>

<style lang="scss" scoped>
.app {
  height: 100vh;
}

.content {
  height: 100%;

  .v-content__wrap {
    overflow: auto;
    padding-bottom: 20px;
    padding-top: 20px;
  }
}
</style>

<script>
import MainLayout from '@/components/layout/main-layout.vue';
export default {
  name: 'App',
  components: {
    MainLayout,
  },
  created() {
    this.$vuetify.theme.dark = true;
  },
};
</script>
