<template>
  <v-app-bar color="secondary" fixed app>
    <v-toolbar-title>
      <v-img :src="require('@/assets/nav_logo.png')" width="45" height="45" contain></v-img>
    </v-toolbar-title>
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
    <v-app-bar-nav-icon class="hidden-md-and-up" color="white" @click.stop="showDrawer()"></v-app-bar-nav-icon>
  </v-app-bar>
</template>

<style scoped>
.v-toolbar__title {
  color: white;
}
</style>

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
  methods: {
    showDrawer() {
      this.$store.commit("toggleDrawer");
    }
  }
};
</script>