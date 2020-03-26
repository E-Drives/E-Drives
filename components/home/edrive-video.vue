<template>
  <section>
    <video controls>
      <source src="~/assets/edrive_video.mp4" type="video/mp4" />
    </video>
  </section>
</template>

<style scoped>
section {
  width: 100vw;
  max-height: calc(100vh - 60px);
}

video {
  width: 100%;
  height: 100%;
  max-height: calc(100vh - 60px);
}
</style>

<script>
export default {
  name: "edrive-video"
};
</script>
