<template>
  <v-container fluid id="whyedrive">
    <v-row align="start" justify="space-around">
      <v-col cols="10" sm="6" md="4" lg="2" xl="2" v-for="item in items" :key="item.title">
        <v-card>
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
  name: "why-edrive",
  data: () => ({
    items: [
      {
        title: "Easy to book",
        text: "Book with just few taps of your phone with seamless payment."
      },
      {
        title: "Economical",
        text: "Our fares are easy on your pocket."
      },
      {
        title: "Never worry about running out of fuel",
        text: "Range is never an excuse, we got 100+km on single charge."
      },
      {
        title: "Quick and fun to ride.",
        text:
          "Bicycle architure allows fantastic maneuverability in jam packed traffic."
      },
      {
        title: "All Electric",
        text: "Moving towards sustainable and greener future."
      }
    ]
  })
};
</script>
