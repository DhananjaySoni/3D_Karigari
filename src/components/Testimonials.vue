<template>
  <div class="testimonials container">
    <h1 class="text-dark">Testimonials</h1>
    <div class="grid-container">
      <div class="grid-item"><img src="/img/testimonials/testi_1.svg" /></div>
      <div class="grid-item"><img src="/img/testimonials/testi_2.svg" /></div>
      <div class="grid-item"><img src="/img/testimonials/testi_3.svg" /></div>
      <div class="grid-item"><img src="/img/testimonials/testi_4.svg" /></div>
      <div class="grid-item"><img src="/img/testimonials/testi_5.svg" /></div>
      <div class="grid-item"><img src="/img/testimonials/testi_6.svg" /></div>
      <div class="grid-item"><img src="/img/testimonials/testi_7.svg" /></div>
      <div class="grid-item"><img src="/img/testimonials/testi_8.svg" /></div>
      <div class="grid-item"><img src="/img/testimonials/testi_9.svg" /></div>
    </div>
  </div>
</template>

<script>
import "vanilla-tilt/dist/vanilla-tilt.js";
export default {
  mounted() {
    const elements = document.querySelectorAll(".grid-item");
VanillaTilt.init(elements,{
  max:30
});

  },
};
</script>

<style lang="scss" scoped>
.testimonials {
  padding-top: 70px;
  .grid-container {
    height: 90%;
    display: grid;
    grid-template-columns: auto auto auto;
    .grid-item {
      background-color: #e6eeec;
      border: 1px solid rgba(141, 137, 137, 0.1);
      filter:drop-shadow(0px 0px 20px rgba(0,0,0,0.1));
      position: relative;      
    }
  }
}
@media (max-width: 767px) {
  .testimonials {
    .grid-container {
      .grid-item {
        img {
          position: absolute;
          left: 0;
          top: 20%;
          margin: auto;
        }
      }
    }
  }
}
</style>