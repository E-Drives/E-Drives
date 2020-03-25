<template>
  <v-app dark>
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
  computed: {
    drawer: {
        get() {
          return this.$store.state.drawer
        },
        set(val) {
          this.$store.commit('drawer', val)
        }
      },
  },
  data() {
    return {
      menu: [
        { icon: "Home", title: "Home" },
        { icon: "Section 1", title: "Section 1", to: "#whyedrive" },
        { icon: "Section 2", title: "Section 2" },
        { icon: "Section 3", title: "Section 3" }
      ]
    };
  }
};
</script>
