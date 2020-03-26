<template>
  <v-footer color="primary">
    <v-container fluid>
      <v-row>
        <v-col cols="6">
          <v-container fluid>
            <p>Connect Via</p>
          </v-container>
          <v-container fluid>
            <v-row>
              <v-col cols="2" v-for="icon in icons" :key="icon.name">
                <v-img :src="getImage(icon.src)" width="24" height="24"></v-img>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
        <v-col cols="6">
          <v-container fluid>
            <p>Download</p>
          </v-container>
          <v-container fluid>
            <!-- // TODO add google play download button and link -->
          </v-container>
        </v-col>
      </v-row>
    </v-container>
    <v-divider></v-divider>
    <v-row>
      <v-col cols="3" v-for="item in items" :key="item.title">
        <v-card flat color="primary">
          <v-card-text class="text-center">{{ item.title }}</v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-footer>
</template>

<style scoped>
.v-card__text,
.v-card__title {
  word-break: normal;
}

.container {
  padding: 0;
}
</style>

<script>
export default {
  name: "edrive-footer",
  data: () => ({
    items: [
      {
        title: "About"
      },
      {
        title: "Terms & Conditions"
      },
      {
        title: "Privacy Policy"
      },
      {
        title: "FAQ"
      }
    ],
    icons: [
      {
        name: "LinkedIn",
        src: "linkedin-brands.svg",
        link: "linkedin.com/company/eco-drives"
      },
      {
        name: "Facebook",
        src: "facebook-square-brands.svg",
        link:
          "https://www.facebook.com/ecodrives.in/?view_public_for=1124549377666418"
      },
      {
        name: "Instagram",
        src: "instagram-square-brands.svg",
        link: " https://www.instagram.com/ecodrives.in/"
      },
      {
        name: "Youtube",
        src: "youtube-square-brands.svg",
        link: "https://www.youtube.com/channel/UC-YkDD2sqoIkoWIcY4qgNcg"
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
