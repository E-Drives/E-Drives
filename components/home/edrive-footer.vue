<template>
  <v-footer color="primary" id="contactus">
    <v-container fluid>
      <v-row>
        <v-col cols="6">
          <v-container fluid>
            <p>Connect Via</p>
          </v-container>
          <v-container fluid>
            <v-row>
              <v-col v-for="icon in icons" :key="icon.name">
                <v-row>
                  <v-spacer></v-spacer>
                  <v-btn text :href="icon.link" target="_blank">
                    <img :src="getImage(icon.src)" width="24" height="24" :class="icon.class" />
                    <p class="hidden-sm-and-down icon-text">{{ icon.name }}</p>
                  </v-btn>
                  <v-spacer></v-spacer>
                </v-row>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
        <v-col cols="6">
          <v-container>
            <v-row class="white--text title" justify="center">Contact</v-row>
            <v-row justify="center">
              Email:-
              <a href="mailto:suraj@ecodrives.in" class="white--text">suraj@ecodrives.in</a>
            </v-row>
            <v-row justify="center">
              Phone No:-
              <a href="tel:8867208322" class="white--text">8867208322</a>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
    <!-- <v-row>
      <v-col cols="3" v-for="item in items" :key="item.title">
        <v-card flat color="primary">
          <v-card-text class="text-center">{{ item.title }}</v-card-text>
        </v-card>
      </v-col>
    </v-row>-->
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

.icon-text {
  margin: 0;
  padding-left: 5px;
}

.img-linkedin {
  filter: invert(26%) sepia(96%) saturate(1491%) hue-rotate(175deg)
    brightness(97%) contrast(101%);
}

.img-facebook {
  filter: invert(34%) sepia(9%) saturate(3641%) hue-rotate(183deg)
    brightness(93%) contrast(89%);
}

.img-youtube {
  filter: invert(25%) sepia(37%) saturate(3293%) hue-rotate(338deg)
    brightness(99%) contrast(99%);
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
        class: "img-linkedin",
        link: "https://linkedin.com/company/eco-drives"
      },
      {
        name: "Facebook",
        src: "facebook-square-brands.svg",
        class: "img-facebook",
        link:
          "https://www.facebook.com/ecodrives.in/?view_public_for=1124549377666418"
      },
      {
        name: "Instagram",
        src: "instagram-logo.png",
        link: " https://www.instagram.com/ecodrives.in/"
      },
      {
        name: "Youtube",
        src: "youtube-square-brands.svg",
        class: "img-youtube",
        link: "https://www.youtube.com/channel/UC-YkDD2sqoIkoWIcY4qgNcg"
      }
    ]
  }),
  methods: {
    getImage(value) {
      return require(`@/assets/footer/${value}`);
    }
  }
};
</script>
