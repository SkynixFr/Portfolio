<template>
  <div class="video-container">
    <iframe
      width="560"
      height="315"
      :src="video.src"
      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
      frameborder="0"
      allowfullscreen
    ></iframe>
  </div>
</template>

<script>
export default {
  name: "Video",
  props: {
    video: {
      type: Object,
      require: true
    }
  }
};
</script>

<style lang="scss" scoped>
.video-container {
  position: relative;
  padding-bottom: 56.25%; /* ratio 16/9 */
  height: 0;
  overflow: hidden;
  clear: both;
}
.video-container iframe,
.video-container object,
.video-container embed {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
