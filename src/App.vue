<template>
    <div id="app">
        <Navbar />
        <ScociaBar />
        <router-view />
        <!-- <div id="fixed-social"> -->
            <!-- <div>
                <a href="#" class="fixed-facebook" target="_blank"><i class="fa fa-facebook-official"></i> <span>Facebook</span></a>
            </div>
            <div>
                <a href="#" class="fixed-twitter" target="_blank"><i class="fa fa-twitter"></i> <span>Twitter</span></a>
            </div>
            <div>
                <a href="#" class="fixed-gplus" target="_blank"><i class="fa fa-google"></i> <span>Google+</span></a>
            </div>
            <div>
                <a href="#" class="fixed-linkedin" target="_blank"><i class="fa fa-linkedin"></i> <span>LinkedIn</span></a>
            </div>
            <div>
                <a href="#" class="fixed-instagrem" target="_blank"><i class="fa fa-instagram"></i> <span>Instagram</span></a>
            </div>
            <div>
                <a href="#" class="fixed-tumblr" target="_blank"><i class="fa fa-tumblr"></i> <span>Tumblr</span></a>
            </div> -->
 
  
    </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import ScociaBar from "@/components/StickySocialBar.vue"
export default {
    components: {
        Navbar,
        ScociaBar
    },
};
</script>
<style scoped>

</style>
<style lang="scss">

// /* fixed social*/
// #fixed-social {
//     position: fixed;
//     top: 35%;
//     // right: 0;
// }

// #fixed-social a {
//     color: #fff;
//     display: block;
//     height: 40px;
//     position: relative;
//     text-align: center;
//     line-height: 40px;
//     width: 40px;
//     margin-bottom: 1px;
//     z-index: 2;
// }
// #fixed-social a:hover > span {
//     visibility: visible;
//     left: 41px;
//     opacity: 1;
// }
// #fixed-social a span {
//     line-height: 40px;
//     left: 60px;
//     position: absolute;
//     text-align: center;
//     width: 120px;
//     visibility: hidden;
//     transition-duration: 0.5s;
//     z-index: 1;
//     opacity: 0;
// }
// .fixed-facebook {
//     background-color: #00aae5;
// }
// .fixed-facebook span {
//     background-color: #00aae5;
// }
// .fixed-twitter {
//     background-color: #7d3895;
// }
// .fixed-twitter span {
//     background-color: #7d3895;
// }
// .fixed-gplus {
//     background-color: #00af54;
// }
// .fixed-gplus span {
//     background-color: #00af54;
// }
// .fixed-linkedin {
//     background-color: #ffc41e;
// }
// .fixed-linkedin span {
//     background-color: #ffc41e;
// }
// .fixed-instagrem {
//     background-color: #ed2b29;
// }
// .fixed-instagrem span {
//     background-color: #ed2b29;
// }
// .fixed-tumblr {
//     background-color: #eb1471;
// }
// .fixed-tumblr span {
//     background-color: #eb1471;
// }
/*end fixed social*/
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    height: 100%;
}

// #nav {
//   padding: 30px;

//   a {
//     font-weight: bold;
//     color: #2c3e50;

//     &.router-link-exact-active {
//       color: #42b983;
//     }
//   }
// }
</style>
