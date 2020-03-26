<template>
  <v-container fluid id="whyedrive">
    <v-container fluid>
      <v-row>
        <v-col>
          <p class="display-1">Why EDrive</p>
        </v-col>
      </v-row>
    </v-container>
    <v-row align="start" justify="space-around">
      <v-col cols="10" sm="6" md="4" xl="2" v-for="item in items" :key="item.title">
        <v-card>
          <v-container>
            <v-img :src="getImage(item.src)"></v-img>
          </v-container>
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
// TODO Resize images
// TODO Make cards consistent and confirm image sizes
export default {
  name: "why-edrive",
  data: () => ({
    items: [
      {
        src: "why_edrive_1.png",
        title: "Easy to book",
        text: "Book with just few taps of your phone with seamless payment."
      },
      {
        src: "why_edrive_2.png",
        title: "Economical",
        text: "Our fares are easy on your pocket."
      },
      {
        src: "why_edrive_3.png",
        title: "Never worry about running out of fuel",
        text: "Range is never an excuse, we got 100+km on single charge."
      },
      {
        src: "why_edrive_4.png",
        title: "Quick and fun to ride.",
        text:
          "Bicycle architure allows fantastic maneuverability in jam packed traffic."
      },
      {
        // TODO Change to Image 5 once given
        src: "why_edrive_4.png",
        title: "All Electric",
        text: "Moving towards sustainable and greener future."
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
