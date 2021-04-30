<template>
    <div>
        <div class="container ">
            <div class="row">
                <div class="col-12 product">
                    <p>
                        Our Products
                    </p>
                </div>
            </div>
            <div class="row">
                <div class="col-12 product">
                    <p>
                        Our Machines
                    </p>
                </div>
            </div>
            <div class="row">
                <div class="col-12 product">
                    <p>
                        Educational Labs
                    </p>
                </div>
            </div>
        </div>
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
    color:#1b4f6a
}
.product {
    margin-top: 6vh;
    font-family: Ginger Bold;
    font-size: 15vh;
    font-weight: 800;
    transition: 1s;
    /* color: ; */
    letter-spacing: 1.5px;
}

.product:hover{
    color: hotpink;
    /* cursor: url(/noz.jpg),default; */
    cursor : url("/cursor/noz.svg"), url("/cursor/noz.cur") 10 12;
    background-image: url("/cursor/noz.jpg");
}

.product:{
    color: rgb(80, 130, 0);
}
@media (max-width: 995px) {
    .product {
        font-size: 10vh;
        margin-top: 10vh;
    }
}
@media (max-width: 400px) {
    .product {
        font-size: 9vh;
        margin-top: 12vh;
    }
}
@media (max-width: 300px) {
    .product {
        font-size: 7vh;
        margin-top: 16vh;
    }
}
</style>
