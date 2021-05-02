<template>
  <div class="home">
    <div class="skw-pages">
      <div class="skw-page skw-page-1 active">
        <div class="skw-page__half skw-page__half--left">
          <div class="skw-page__skewed">
            <div class="video-container">
              <video id="homeVid" keepplaying="true" loop autoPlay muted>
                <source src="/clock.mp4" type="video/mp4" />
              </video>
            </div>
          </div>
        </div>
      </div>
      <div class="skw-page skw-page-2">
        <div class="skw-page__half skw-page__half--left">
          <div class="skw-page__skewed">
            <div class="skw-page__content">
              <div class="about container">
                <div class="row">
                  <div class="col-md-6 col-12 col">
                    <img src="/img/3d_about_1.jpg" class="rounded shadow" />
                  </div>
                  <div class="col-md-6 col-12 col">
                    <div class="about_content">
                      <h1>What is 3D?</h1>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiumdod tempor incididunt ut labore et dolore
                        magna aliqua. Ut enim ad minim veniam, quis nostrud
                        exercitation ullamco laboris nisi ut aliquip ex ea
                        commodo consequat. Duis aute irure dolor in
                        reprehenderit in voluptate
                      </p>
                    </div>
                  </div>
                </div>
                <div class="row">
                  <div class="col-md-6 col-12 col">
                    <div class="about_content">
                      <h1>What is 3DKarigari?</h1>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiumdod tempor incididunt ut labore et dolore
                        magna aliqua. Ut enim ad minim veniam, quis nostrud
                        exercitation ullamco laboris nisi ut aliquip ex ea
                        commodo consequat. Duis aute irure dolor in
                        reprehenderit in voluptate
                      </p>
                    </div>
                  </div>
                  <div class="col-md-6 col-12 col">
                    <img src="/img/3d_about_1.jpg" class="rounded shadow" />
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="skw-page skw-page-3">
        <div class="skw-page__half skw-page__half--left">
          <div class="skw-page__skewed">
            <div class="skw-page__content">
              <Testimonials/>
            </div>
          </div>
        </div>
      </div>
      <div class="skw-page skw-page-4">
        <div class="skw-page__half skw-page__half--left">
          <div class="skw-page__skewed">
            <div class="skw-page__content"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import Testimonials from "@/components/Testimonials.vue";
import Footer from "@/components/Footer.vue";
import $ from "jquery";
export default {
  name: "Home",
  components: {
    Testimonials,
    Footer,
  },
  mounted() {
    var curPage = 1;
    var numOfPages = $(".skw-page").length;
    var animTime = 1000;
    var scrolling = false;
    var pgPrefix = ".skw-page-";

    function pagination() {
      scrolling = true;

      $(pgPrefix + curPage)
        .removeClass("inactive")
        .addClass("active");
      $(pgPrefix + (curPage - 1)).addClass("inactive");
      $(pgPrefix + (curPage + 1)).removeClass("active");

      setTimeout(function () {
        scrolling = false;
      }, animTime);
    }

    function navigateUp() {
      if (curPage === 1) return;
      curPage--;
      pagination();
    }

    function navigateDown() {
      if (curPage === numOfPages) return;
      curPage++;
      pagination();
    }

    $(document).on("mousewheel DOMMouseScroll", function (e) {
      if (scrolling) return;
      if (e.originalEvent.wheelDelta > 0 || e.originalEvent.detail < 0) {
        navigateUp();
      } else {
        navigateDown();
      }
    });

    $(document).on("keydown", function (e) {
      if (scrolling) return;
      if (e.which === 38) {
        navigateUp();
      } else if (e.which === 40) {
        navigateDown();
      }
    });
  },
};
</script>


<style lang='scss' scoped>
$openSans: "Open Sans", Helvetica, Arial, sans-serif;

.skw-pages {
  overflow: hidden;
  position: relative;
  height: 100vh;
}

$scrollTime: 1s;

.skw-page {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;

  &__half {
    width: 100%;
    height: 100vh;
    transition: transform $scrollTime;

    &--left {
      left: 0;
      transform: translate3d(0, 100%, 0);
    }

    .skw-page.active & {
      transform: translate3d(0, 0, 0);
    }
  }

  &__skewed {
    overflow: hidden;
    width: 100%;
    height: 100%;
    background: #000;
  }

  &__content {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-flow: column wrap;
    width: 100%;
    height: 100%;
    color: #fff;
    transition: transform $scrollTime, opacity $scrollTime;
    background-size: cover;

    .skw-page__half--left & {
      transform-origin: 100% 0;
    }

    .skw-page.inactive & {
      opacity: 0.5;
      transform: translate3d(0, -100%, 0);
    }
  }

  &-2 {
    .skw-page__half--left .skw-page__content {
      background: rgb(247, 101, 48);
      padding-top: 70px;
      padding-bottom: 10px;
      .about {
        height: 100%;
        width: 100%;
        .row {
          height: 50%;
          .col {
            max-height: 100%;
            object-fit: cover;
            .about_content {
              padding: 10% 3%;
              p {
                font-size: 18px;
                text-align: justify;
              }
            }
            img {
              height: 100%;
              width: 90%;
            }
          }
        }
      }
    }
  }
  &-3 {
    .skw-page__half--left .skw-page__content {
      background: #e6eeec;
      overflow:hidden;
    }
  }
  &-4 {
    .skw-page__half--left .skw-page__content {
      background: lighten(#1c1c1c, 5%);
    }
  }
}

@media (max-width: 768px) {
  .skw-page {
    &-2 {
      .skw-page__half--left .skw-page__content {
        background: rgb(247, 101, 48);
        padding-top: 70px;
        padding-bottom: 10px;
        .about {
          height: 100%;
          width: 100%;
          .row {
            height: 100%;
            .col {
              max-height: 50%;
              .about_content{
                padding-top:0;
                p {
                font-size: 16px;
              }
              }
              img {
                padding-top:5%;
                max-width: 100%;
                height: auto;
              }
            }
          }
        }
      }
    }
  }
}

.video-container {
  // position: absolute;
  // top: 0;
  // left: 0;
  width: 100%;
  height: 100vh;
  -webkit-overflow-scrolling: touch;
}
.video-container > video {
  display: block;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  z-index: 1;
}
</style>