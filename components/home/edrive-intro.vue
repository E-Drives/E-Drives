<template>
  <div id="intro">
    <v-container class="main-container" fluid>
      <v-row justify="center" align="center">
        <v-col cols="8" sm="6">
          <v-container>
            <v-row>
              <v-col lg="4" md="5" sm="6" cols="8">
                <v-row justify="center">
                  <img
                    class="img-responsive justify-center"
                    :src="require('@/assets/logo/edrive_logo.png')"
                    alt="Edrive"
                  />
                  <span class="white--text">"IMPROVING LIVES"</span>
                </v-row>
              </v-col>
            </v-row>
          </v-container>
          <v-container>
            <v-row
              class="white--text"
            >We're a team of riders, designers, dreamers and doers. We might have different job titles, but we are reunited by one goal: to help delivery partners do their deliveries in style and save some money.</v-row>
          </v-container>
          <v-container>
            <a
              href="https://play.google.com/store/apps/details?id=com.ecodrives.ecodrive"
              target="_blank"
              text
            >
              <v-img :src="require('@/assets/intro/google-play-badge.png')" width="200" height="60"></v-img>
            </a>
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
    max-height: 131.5px;
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