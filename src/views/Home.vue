<template>
  <div class="home">
    <Navbar />
    <section class="page1">
      <video id="homeVid" keepplaying="true" loop autoPlay muted height="100%" width="100%">
        <source src="/clock.mp4" type="video/mp4" />
      </video>
    </section>
    <section class="page2"></section>
    <section class="page3">

      <Footer/>
    </section>
    
  </div>
</template>


<script>
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
import $ from "jquery";
export default {
  name: "Home",
  components: {
    Navbar,
    Footer
  },
  mounted() {
    $(".home").onepage_scroll({
      sectionContainer: "section",
      easing: "ease",
      animationTime: 1000,
      pagination: true,
      updateURL: false,
      beforeMove: function (index) {},
      afterMove: function (index) {},
      loop: false,
      keyboard: true,
      responsiveFallback: false,
      direction: "vertical",
    });
  },
};
</script>
<style lang='scss' scoped>
// onepage-pagination {
  
//     list-style-type: upper-roman !important;
  
// }
section {
  height: 100vh;
  width: 100%;
}
.page1 {
  background: #000;
}
.page2 {
  background: #f8b333;
}
.page3 {
  background: #e6eeec;
}
</style>