<template>
  <v-app-bar color="secondary" fixed app>
    <v-toolbar-title>
      <v-img :src="require('@/assets/logo/edrive_logo.png')" width="45" height="45" contain></v-img>
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
        { icon: "Home", title: "Home", to: "#intro" },
        { icon: "Why E Drives", title: "Why E Drives", to: "#whyedrives" },
        { icon: "How To Book", title: "How To Book", to: "#howedrives" },
        { icon: "Contact Us", title: "Contact Us", to: "#contactus" }
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