<template>
  <div id="wrap_hobbies">
    <h1>Interest</h1>
    <div class="title_boder"></div>
    <b-carousel
    class="interest_wrap"
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"
    fade
    v-model="slide"
    :interval="3000"
    controls
    indicators
    img-width="1024"
    img-height="480"
  >
    <b-carousel-slide
      caption="2022台灣祭"
      img-src="https://res.cloudinary.com/dar3kgszx/image/upload/v1662300254/%E5%8F%B0%E7%81%A3%E7%A5%AD_drwlay.jpg"
    ></b-carousel-slide>
    <b-carousel-slide
      caption="2022諸羅祭"
      img-src="https://res.cloudinary.com/dar3kgszx/image/upload/v1662303016/sorryyoung22_mfc0xk.jpg"
    ></b-carousel-slide>
    <b-carousel-slide
      caption="deca joins小巡迴"
      img-src="https://res.cloudinary.com/dar3kgszx/image/upload/v1662303109/decajoins11_qv23l2.jpg"
    ></b-carousel-slide>
  </b-carousel>
  </div>
</template>
<style>
.interest_wrap{
  margin-top: 70px;
}

</style>
<script>
  export default {
    data() {
      return {
        slide: 0,
        sliding: null
      }
    },
    methods: {
      onSlideStart(slide) {
        this.sliding = true
      },
      onSlideEnd(slide) {
        this.sliding = false
      }
    }
  }
</script>
