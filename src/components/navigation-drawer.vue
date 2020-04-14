<template>
  <v-navigation-drawer
    :mini-variant.sync="mini"
    app
    clipped
    permanent
    :v-model="drawer"
  >
    <v-list>
      <v-list-item>
        <v-btn icon @click.stop="mini = !mini">
          <v-icon v-if="mini">mdi-unfold-more-vertical</v-icon>
          <v-icon v-else>mdi-unfold-less-vertical</v-icon>
        </v-btn>
      </v-list-item>
    </v-list>
    <v-divider></v-divider>
    <v-list dense nav>
      <v-list-item v-for="item in items" :key="item.title" link>
        <v-list-item-icon>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>
<script>
export default {
  data() {
    return {
      items: [
        { title: 'Dashboard', icon: 'mdi-view-dashboard' },
        { title: 'Photos', icon: 'mdi-image' },
        { title: 'About', icon: 'mdi-help-box' },
      ],
      drawer: true,
      mini: true,
    };
  },
};
</script>
