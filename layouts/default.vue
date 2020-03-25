<template>
  <v-app dark>
    <v-app-bar color="secondary" fixed app>
      <v-toolbar-title></v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn
          v-for="item in menu"
          :key="item.icon"
          text
          color="white"
          :href="item.to"
        >{{ item.title }}</v-btn>
      </v-toolbar-items>
      <v-app-bar-nav-icon class="hidden-md-and-up" color="white" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
    </v-app-bar>
    <v-content>
      <nuxt />
    </v-content>
    <v-navigation-drawer right temporary fixed v-model="drawer">
      <v-list>
        <v-list-item v-for="item in menu" :key="item.icon">
          <v-list-item-action-text>{{ item.title }}</v-list-item-action-text>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      menu: [
        { icon: "Home", title: "Home" },
        { icon: "Section 1", title: "Section 1", to: "#whyedrive" },
        { icon: "Section 2", title: "Section 2" },
        { icon: "Section 3", title: "Section 3" }
      ]
    };
  },
};
</script>
