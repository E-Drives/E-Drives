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
      <v-tab-item>FAQ</v-tab-item>
      <v-tab-item>Contact Us</v-tab-item>
    </v-tabs>
  </div>
</template>

<script>
export default {
  name: "tabbar"
};
</script>