<template>
  <v-app dark>
    <AppBar></AppBar>
    <v-content>
      <nuxt />
    </v-content>
    <v-navigation-drawer right temporary fixed v-model="drawer">
      <v-list>
        <template v-for="item in menu">
          <v-list-item :key="item.icon" :to="item.to">
            <v-list-item-action-text>{{ item.title }}</v-list-item-action-text>
          </v-list-item>
        </template>
      </v-list>
    </v-navigation-drawer>
  </v-app>
</template>

<script>
import AppBar from "~/components/home/appbar";

export default {
  components: {
    AppBar
  },
  computed: {
    drawer: {
      get() {
        return this.$store.state.drawer;
      },
      set(val) {
        this.$store.commit("drawer", val);
      }
    }
  },
  data() {
    return {
      menu: [
        { icon: "Home", title: "Home", to: "#intro" },
        { icon: "Why E Drives", title: "Why E Drives", to: "#whyedrives" },
        { icon: "How To Book", title: "How To Book", to: "#howedrives" },
        { icon: "Contact Us", title: "Contact Us", to: "#contactus" }
      ]
    };
  }
};
</script>
