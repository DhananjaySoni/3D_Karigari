<template>
    <div class="productsMain">
        <div class="container">
            <div class="row">
                <div class="col-12 product">
                    <p v-b-modal.modal-scrollable class="product">
                        Our Products
                    </p>
                </div>
            </div>
            <div class="row emoji">
                <div class="col-12 product ">
                    <p v-b-modal.modal-scrollable class="product">
                        Our Machines
                    </p>
                </div>
            </div>
            <div class="row ">
                <div class="col-12 product">
                    <p v-b-modal.modal-scrollable class="product">
                        Educational Labs
                    </p>
                </div>
            </div>
        </div>
        <b-modal id="modal-scrollable" scrollable size="xl" hide-footer>
            <p class="my-4" v-for="i in 20" :key="i">
                Cras mattis consectetur purus sit amet fermentum. 
                Cras justo odio, dapibus ac facilisis in, egestas eget quam. 
                Morbi leo risus, porta ac consectetur ac, vestibulum at eros.
            </p>
        </b-modal>
    </div>
</template>

<script>
export default {};
</script>

<style>
.container {
    /* margin-top:8vh; */
    height: 100vh;
}
.bg {
    background-color: coral;
    color: #1b4f6a;
}
.product {
    margin-top: 5vh;
    font-family: Ginger Bold;
    font-size: 11vh;
    font-weight: 800;
    transition: 1s;
    /* color: ; */
    letter-spacing: 1.5px;
}

.product:hover {
    color: rgb(226, 21, 123);
    /* cursor: url(/noz.jpg),default; */
    /* cursor : url(/cursor/noz.svg),20 20, auto; */
    /* background-image: url("/cursor/noz.jpg"); */
    cursor: url(https://abs.twimg.com/emoji/v2/72x72/1f525.png) 36 36, auto;
}
/* .emoji {
} */

.product {
    color: rgb(22, 100, 87);
}
@media (max-width: 1050px) {
    .product {
        font-size: 9vh;
        margin-top: 10vh;
    }
}
@media (max-width: 995px) {
    .product {
        font-size: 10vh;
        margin-top: 10vh;
    }
}
@media (max-width: 520px) {
    .product {
        font-size: 6.5vh;
        margin-top: 12vh;
    }
}
@media (max-width: 350px) {
    .product {
        font-size: 5vh;
        margin-top: 16vh;
    }
}
</style>
