<template>
    <div class="bg">
        <navbar />
        <ProductPage />
        <Footer />
    </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
import ProductPage from "@/components/ProductPage.vue"

export default {
    components: {
        Footer,
        Navbar,
        ProductPage,
    },
};
</script>

<style>

</style>
