<template>
  <v-footer color="secondary" id="contactus">
    <v-container fluid class="hidden-xs-only">
      <v-row justify="space-around">
        <v-cols sm="4">
          <v-card flat color="secondary">
            <v-card-title class="justify-center white--text title">Connect Via</v-card-title>
            <v-row v-for="icon in icons" :key="icon.name">
              <v-btn text :href="icon.link" target="_blank">
                <img :src="getImage(icon.src)" width="24" height="24" :class="icon.class" />
                <p class="icon-text white--text">{{ icon.name }}</p>
              </v-btn>
            </v-row>
          </v-card>
        </v-cols>
        <v-cols sm="4">
          <v-card flat color="secondary">
            <v-card-title class="justify-center white--text title">E Drives Details</v-card-title>
            <v-row v-for="item in items" :key="item.title" justify="center">
              <v-btn text :href="item.href">
                <span class="white--text">{{ item.title }}</span>
              </v-btn>
            </v-row>
          </v-card>
        </v-cols>
        <v-cols sm="4">
          <v-card flat color="secondary">
            <v-card-title class="justify-center white--text title">Contact</v-card-title>
            <v-row>
              <v-btn text>
                Email:-&nbsp;
                <a
                  href="mailto:suraj@ecodrives.in"
                  class="white--text"
                >suraj@ecodrives.in</a>
              </v-btn>
            </v-row>
            <v-row>
              <v-btn text>
                Phone No:-&nbsp;
                <a href="tel:8867208322" class="white--text">8867208322</a>
              </v-btn>
            </v-row>
            <v-row>
              <v-container>
                <v-row justify="center">
                  <a
                    href="https://play.google.com/store/apps/details?id=com.ecodrives.ecodrive"
                    target="_blank"
                    text
                  >
                    <v-img
                      :src="require('@/assets/intro/google-play-badge.png')"
                      width="200"
                      height="60"
                    ></v-img>
                  </a>
                </v-row>
              </v-container>
            </v-row>
          </v-card>
        </v-cols>
      </v-row>
    </v-container>
    <v-container fluid class="hidden-sm-and-up">
      <v-container fluid>
        <v-row justify="center">
          <v-cols>
            <v-card flat color="secondary">
              <v-card-title class="justify-center white--text title">Contact</v-card-title>
              <v-row>
                <v-btn text>
                  Email:-&nbsp;
                  <a
                    href="mailto:suraj@ecodrives.in"
                    class="white--text"
                  >suraj@ecodrives.in</a>
                </v-btn>
              </v-row>
              <v-row>
                <v-btn text>
                  Phone No:-&nbsp;
                  <a href="tel:8867208322" class="white--text">8867208322</a>
                </v-btn>
              </v-row>
              <v-row>
                <v-container>
                  <v-row justify="center">
                    <a
                      href="https://play.google.com/store/apps/details?id=com.ecodrives.ecodrive"
                      target="_blank"
                      text
                    >
                      <v-img
                        :src="require('@/assets/intro/google-play-badge.png')"
                        width="200"
                        height="60"
                      ></v-img>
                    </a>
                  </v-row>
                </v-container>
              </v-row>
            </v-card>
          </v-cols>
        </v-row>
      </v-container>
      <div style="height: 25px"></div>
      <v-container fluid>
        <v-row justify="center">
          <span class="white--text">Connect Via</span>
        </v-row>
        <v-row justify="space-around">
          <v-btn
            large
            text
            class="white--text"
            v-for="icon in icons"
            :key="icon.name"
            :href="icon.link"
          >
            <img :src="getImage(icon.src)" width="24" height="24" :class="icon.class" />
          </v-btn>
        </v-row>
      </v-container>
      <div style="height: 25px"></div>
      <v-container fluid>
        <v-row justify="center">
          <v-btn
            x-small
            text
            class="white--text"
            v-for="item in items"
            :key="item.title"
            :href="item.href"
          >{{ item.title }}</v-btn>
        </v-row>
      </v-container>
    </v-container>
    <v-container>
      <v-row
        justify="center"
        class="white--text"
      >&copy; {{ new Date().getFullYear() }} EDIMV PVT LTD</v-row>
    </v-container>
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
        title: "Terms & Conditions",
        href: "/terms_and_conditions"
      },
      {
        title: "Privacy Policy",
        href: "/privacy_policy"
      },
      {
        title: "FAQ",
        href: "faq"
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
        link: " https://www.instagram.com/edrives.in/"
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
