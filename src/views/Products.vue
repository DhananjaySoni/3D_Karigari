<template>
  <div class="products">
    <div class="bg">
      <ProductPage />
      <Footer />
    </div>
  </div>
</template>

<script>
import Footer from "@/components/Footer.vue";
import ProductPage from "@/components/ProductPage.vue";

export default {
  components: {
    Footer,
    ProductPage,
  },
};
</script>

