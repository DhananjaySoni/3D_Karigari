<template>
  <div class="testimonials container">
    <h1 class="text-dark">Testimonials</h1>
    <div class="grid-container-root">
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
  </div>
</template>

<script>
import "vanilla-tilt/dist/vanilla-tilt.js";
export default {
  mounted() {
    const elements = document.querySelectorAll(".grid-item");
    VanillaTilt.init(elements, {
      max: 30,
    });
  },
};
</script>

<style lang="scss" scoped>
.testimonials {
  padding-top: 70px;
  overflow:hidden;
  .grid-container-root {
    height:90%;
    width:100%;
    .grid-container {
      height: 90%;
      display: grid;
      grid-template-columns: auto auto auto;
      .grid-item {
        background-color: #e6eeec;
        border: 1px solid rgba(141, 137, 137, 0.1);
        filter: drop-shadow(0px 0px 10px rgba(0, 0, 0, 0.1));
        position: relative;
      }
    }
  }
}
@media (max-width: 992px) {
  .testimonials {
    .grid-container-root {
      .grid-container {
        .grid-item {
          img {
            position: absolute;
            left: 0;
            top: 0;
            bottom:0;
            margin: auto;
          }
        }
      }
    }
  }
}

@media (max-width: 450px) {
  .testimonials {
    padding-top:100px;
    .grid-container-root {
      // padding-top:7vh;
      .grid-container {
        margin-top:20px;
        height: 80%;
      }
    }
  }
}
</style>