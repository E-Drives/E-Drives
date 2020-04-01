<template>
  <div>
    <v-container class="main-container" fluid>
      <v-row justify="center" align="center">
        <v-col cols="8" sm="6">
          <v-container>
            <v-row>
              <v-container>
                <div class="img-center">
                  <img
                    class="img-responsive justify-center"
                    :src="require('@/assets/logo/edrive_logo.png')"
                    alt="Edrive"
                  />
                </div>
                <span class="white--text">IMPROVING LIVES</span>
              </v-container>
            </v-row>
          </v-container>
          <v-container>
            <v-row
              class="white--text"
            >We're a team of riders, designers, dreamers and doers. We might have different job titles, but we are reunited by one goal: to help delivery partners do their deliveries in style and save some money.</v-row>
          </v-container>
          <v-container>
            <v-row class="white--text">Contact Suraj:</v-row>
            <v-row>
              Email:-
              <a href="mailto:suraj@ecodrives.in" class="white--text">suraj@ecodrives.in</a>
            </v-row>
            <v-row>
              Phone No:-
              <a href="tel:8867208322" class="white--text">8867208322</a>
            </v-row>
          </v-container>
        </v-col>
        <v-col cols="8" sm="4">
          <img class="img-col-responsive" :src="require('@/assets/intro/edrive_intro_beta.png')" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<style lang="scss" scoped>
.main-container {
  background-color: #95c93d;

  .img-responsive {
    width: 100px;
    height: auto;
  }

  .img-col-responsive {
    width: 100%;
  }
}
</style>

<script>
export default {
  name: "edrive-intro"
};
</script>