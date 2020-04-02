<template>
  <v-container fluid id="whyedrives">
    <v-container fluid>
      <v-row>
        <v-col>
          <span class="display-1 sec-head white--text">Why E Drives</span>
        </v-col>
      </v-row>
    </v-container>
    <v-row align="start" justify="space-around">
      <v-col cols="8" sm="4" md="2" v-for="item in items" :key="item.title">
        <v-card flat>
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

.sec-head {
  background-color: #95c93d;
  padding: 10px;
  border-radius: 12px;
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
        src: "why_edrive_5.png",
        title: "All Electric",
        text: "Moving towards sustainable and greener future."
      }
    ]
  }),
  methods: {
    getImage(value) {
      return require(`@/assets/why_edrive/${value}`);
    }
  }
};
</script>
