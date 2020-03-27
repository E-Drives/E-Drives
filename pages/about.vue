<template>
  <div>
    <v-tabs background-color="primary" fixed-tabs>
      <v-tab>About</v-tab>
      <v-tab>Terms & Conditions</v-tab>
      <v-tab>Privacy Policy</v-tab>
      <v-tab>FAQ</v-tab>
      <v-tab>Contact Us</v-tab>

      <v-tab-item>About</v-tab-item>
      <v-tab-item>Terms & Conditions</v-tab-item>
      <v-tab-item>Privacy Policy</v-tab-item>
      <v-tab-item>
        <FaqEdrive></FaqEdrive>
      </v-tab-item>
      <v-tab-item>Contact Us</v-tab-item>
    </v-tabs>
  </div>
</template>

<script>
import FaqEdrive from "~/components/about/faq-edrive";

export default {
  name: "tabbar",
  components: {
    FaqEdrive
  }
};
</script>