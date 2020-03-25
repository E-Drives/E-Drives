<template>
  <div>
    <AppBar></AppBar>
    <WhyEdrive></WhyEdrive>
    <EdriveVideo></EdriveVideo>
  </div>
</template>

<style scoped>
</style>

<script>
import AppBar from "~/components/appbar";
import EdriveVideo from "~/components/edrive-video";
import WhyEdrive from "~/components/why-edrive";

export default {
  components: {
    AppBar,
    WhyEdrive,
    EdriveVideo
  }
};
</script>
