<template>
  <div>
    <EdriveIntro></EdriveIntro>
    <WhyEdrive></WhyEdrive>
    <HowEdrive></HowEdrive>
    <EdriveVideo></EdriveVideo>
    <EdriveTestimonial></EdriveTestimonial>
    <EdriveFooter></EdriveFooter>
  </div>
</template>

<style scoped>
</style>

<script>
import EdriveIntro from "~/components/home/edrive-intro";
import WhyEdrive from "~/components/home/why-edrive";
import HowEdrive from "~/components/home/how-edrive";
import EdriveVideo from "~/components/home/edrive-video";
import EdriveTestimonial from "~/components/home/edrive-testimonial";
import EdriveFooter from "~/components/home/edrive-footer";

export default {
  components: {
    EdriveIntro,
    WhyEdrive,
    HowEdrive,
    EdriveVideo,
    EdriveTestimonial,
    EdriveFooter
  }
};
</script>
