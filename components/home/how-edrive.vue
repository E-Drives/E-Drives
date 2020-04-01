<template>
  <v-container fluid>
    <v-container fluid>
      <v-row>
        <v-col>
          <span class="display-1 sec-head white--text">How eDrive</span>
        </v-col>
      </v-row>
    </v-container>
    <v-row justify="center" align="center">
      <v-col cols="7" sm="6">
        <v-row justify="center" align="center">
          <img
            class="img-responsive"
            :src="require('@/assets/how_edrive/how_edrive.png')"
            alt="How Edrive"
          />
        </v-row>
      </v-col>
      <v-col cols="8" sm="6">
        <v-row v-for="(item, index) in items" :key="index">
          <v-card flat>
            <v-card-title>{{ item.title }}</v-card-title>
            <v-card-subtitle>{{ item.text }}</v-card-subtitle>
          </v-card>
        </v-row>
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

.img-responsive {
  width: 300px;
}

@media all and (max-width: 600px) {
  .img-responsive {
    width: 215px;
  }
}
</style>

<script>
export default {
  name: "how-edrive",
  data: () => ({
    items: [
      {
        title: "Download the E drives App.",
        text: "Download the app from Google play."
      },
      {
        title: "Book your Ride:",
        text:
          "Select your Booking dates and pick your vehicle from your nearest pickup point."
      },
      {
        title: "Ride safely:",
        text:
          "Enjoy E drives ride, but remember to abide by all the traffic laws and parking policies."
      },
      {
        title: "End your Ride:",
        text: "Return back to our nearest drop point."
      }
    ]
  })
};
</script>