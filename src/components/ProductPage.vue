<template>
    <div class="productsMain">
        <div class="container">
            <div class="row">
                <div class="col-12 product my-auto">
                    <a href="#" v-b-modal.modal-scrollable> Our Products </a>
                </div>
            </div>
            <div class="row">
                <div class="col-12 product my-auto">
                    <a href="#" v-b-modal.modal-scrollable> Our Machines </a>
                </div>
            </div>
            <div class="row">
                <div class="col-12 product my-auto">
                    <a href="#" v-b-modal.modal-scrollable> Educational Labs </a>
                </div>
            </div>
        </div>
        <b-modal id="modal-scrollable" scrollable size="xl" hide-footer>
            <div class="my-4 Flex" v-for="i in 20" :key="i">
                <div>
                    <b-card title="Card Title" img-src="https://picsum.photos/600/300/?image=25" img-alt="Image" img-top tag="article" style="max-width: 20rem" class="mb-2">
                        <b-card-text>
                            Some quick example text to build on the card title and make up the bulk of the card's content.
                        </b-card-text>
                        <b-button href="#" variant="primary">Enquire Me</b-button>
                    </b-card>
                </div>
                <div>
                    <b-card title="Card Title" img-src="https://picsum.photos/600/300/?image=25" img-alt="Image" img-top tag="article" style="max-width: 20rem;" class="mb-2">
                        <b-card-text>
                            Some quick example text to build on the card title and make up the bulk of the card's content.
                        </b-card-text>

                        <b-button href="#" variant="primary">Go somewhere</b-button>
                    </b-card>
                </div>
                <div>
                    <b-card title="Card Title" img-src="https://picsum.photos/600/300/?image=25" img-alt="Image" img-top tag="article" style="max-width: 20rem;" class="mb-2">
                        <b-card-text>
                            Some quick example text to build on the card title and make up the bulk of the card's content.
                        </b-card-text>

                        <b-button href="#" variant="primary">Go somewhere</b-button>
                    </b-card>
                </div>
            </div>
        </b-modal>
    </div>
</template>

<style>
.container {
    height: 100%;
}
.Flex {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    flex-wrap: wrap;
}
.bg {
    background-color: coral;
    color: #1b4f6a;
}
.productsMain {
    height: 100vh;
    padding-top: 70px;
    padding-bottom: 8vh;
}

.row {
    height: 30%;
    overflow: hidden;
}

.product {
    /* font-family: Ginger Bold; */
    font-size: 15vh;
    font-weight: 800;
    line-height: 15vh;
    letter-spacing: 1.5px;
}
.product a {
    width: auto;
    transition: 1s;
    color: rgb(0, 0, 0);
    display: inline-block;
}
.product a:hover {
    text-decoration: none;
    color: rgb(155, 6, 81);
    transform: scale(1.1);
    cursor: url(data:image/png;base64,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), auto;
}

@media (max-width: 1050px) {
    .productsMain {
        height: 90vh;
    }
    .product {
        font-size: 13vh;
        line-height: 13vh;
    }
}

@media (max-width: 995px) {
    .product a {
        font-size: 10vh;
        line-height: 10vh;
    }
}
@media (max-width: 500px) {
    .product a {
        font-size: 7vh;
        line-height: 8vh;
    }
}
@media (max-width: 300px) {
    .product a {
        font-size: 5vh;
        line-height: 5vh;
    }
}
</style>
