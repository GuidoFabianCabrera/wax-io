<template>
  <section class="video">
    <div class="video__container">
      <!-- <iframe
        width="100%"
        height="100%"
        src="https://www.youtube.com/embed/wPDiEw66vTU?controls=0&mute=1&rel=0&loop=1&modestbranding=1&showinfo=0&controls=0&iv_load_policy=3&autohide=1&autoplay=1&disablekb=1&fs=0&html5=1&enablejsapi=1"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture;"
        allowfullscreen
      ></iframe> -->
      <video
        class="video__link video__link--desktop"
        src="images/video.webm"
        autoplay
        loop
        muted
        width="100%"
        height="100%"
      ></video>
      <video
        class="video__link video__link--mobile"
        src="images/video-mobile.webm"
        autoplay
        loop
        muted
        width="100%"
        height="100%"
      ></video>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.video {
  background-color: black;

  .video__container {
    padding-top: 15px;
    padding-bottom: 15px;

    width: 320px;
    height: 600px;
    margin: 0 auto;

    // border: 1px solid red;

    @include breakpoint(sm) {
      width: 620px;
    }

    @include breakpoint(md) {
      width: auto;
      padding-top: 0;
      padding-bottom: 0;
    }
  }

  .video__link {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .video__link--desktop {
    display: none;
    @include breakpoint(md) {
      display: block;
    }
  }

  .video__link--mobile {
    display: block;
    @include breakpoint(md) {
      display: none;
    }
  }
}
</style>
