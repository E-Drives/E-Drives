<template>
  <v-container fluid>
    <v-container fluid>
      <v-row>
        <v-col>
          <span class="display-1 sec-head white--text">Testimonials</span>
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid>
      <v-row>
        <v-col cols="12" md="6">
          <v-carousel height="400" show-arrows-on-hover>
            <v-carousel-item v-for="(slide, index) in slides" :key="index">
              <v-sheet color="secondary" height="100%">
                <v-row justify="center" align="center" class="fill-height">
                  <v-col>
                    <v-row justify="center" align="center">
                      <v-avatar size="175">
                        <img :src="getImage(slide.src)" width="175" height="175" />
                      </v-avatar>
                    </v-row>
                    <v-row justify="center" align="center">
                      <div
                        :class="{ 'title': $vuetify.breakpoint.xs, 'headline': $vuetify.breakpoint.smAndUp}"
                      >{{ slide.title }}</div>
                    </v-row>
                    <v-row justify="center" align="center">
                      <div
                        :class="{'text-body-sm': $vuetify.breakpoint.smAndUp, 'text-body': $vuetify.breakpoint.xs, 'body-1': $vuetify.breakpoint.smAndUp}"
                      >
                        <div class="text-center">{{ slide.text }}</div>
                      </div>
                    </v-row>
                  </v-col>
                </v-row>
              </v-sheet>
            </v-carousel-item>
          </v-carousel>
        </v-col>
        <v-col cols="12" md="6">
          <iframe
            class="vid-responsive"
            src="https://www.youtube.com/embed/sG2Mkx8aLUs"
            frameborder="0"
            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </v-col>
      </v-row>
    </v-container>
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

.text-body {
  width: 300px;
}

.text-body-sm {
  width: 300px;
}

.vid-responsive {
  width: 100%;
  height: 100%;
}

@media all and (max-width: 960px) {
  .vid-responsive {
    min-height: 500px;
  }
}

@media all and (max-width: 600px) {
  .vid-responsive {
    min-height: 300px;
  }
}
</style>

<script>
export default {
  name: "edrive-testimonial",
  data: () => ({
    slides: [
      {
        src: "umesh_ji.jpg",
        title: "Mr. Umesh (Zomato)",
        text: "My monthly expenditure on vehicle have been reduced by 50%."
      },
      {
        src: "rakesh_ji.jpg",
        title: "Mr. Rakesh (Swiggy)",
        text:
          "It’s quick & fun to ride, it gives fantastic maneuverability in jam packed traffic."
      }
    ]
  }),
  methods: {
    getImage(value) {
      return require(`@/assets/testimonials/${value}`);
    }
  }
};
</script>