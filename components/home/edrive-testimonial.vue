<template>
  <v-container fluid>
    <v-container fluid>
      <v-row>
        <v-col>
          <p class="display-1">Testimonials</p>
        </v-col>
      </v-row>
    </v-container>
    <v-row align="start" justify="space-around">
      <v-col cols="8" sm="5" v-for="item in items" :key="item.title">
        <v-card>
          <v-img :src="getImage(item.src)"></v-img>
          <v-card-title>{{ item.title }}</v-card-title>
          <v-card-text>{{ item.text }}</v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.v-card__text,
.v-card__title {
  word-break: normal;
}
</style>

<script>
export default {
  name: "edrive-testimonial",
  data: () => ({
    items: [
      {
        src: "umesh_ji.jpg",
        title: "MR. Umesh (Zomato)",
        text: "My monthly expenditure on vehicle have been reduced by 50%."
      },
      {
        src: "rakesh_ji.jpg",
        title: "Mr.Rakesh (Swiggy)",
        text:
          "It’s quick & fun to ride, it gives fantastic maneuverability in jam packed traffic."
      }
    ]
  }),
  methods: {
    getImage(value) {
      return require(`@/assets/${value}`);
    }
  }
};
</script>