<script>

import CardComponent from './CardComponent.vue'

export default {

    components: {
        CardComponent
    }, 

    data() {
        return {
            products: [
                {
                    id: 1,
                    frontImage: "1.webp",
                    backImage: "1b.webp",
                    brand: "Levi's",
                    name: "Relaxed Fit",
                    price: 29.99,
                    isInFavorites: true,
                    badges: [
                        {
                            type: "tag",
                            value: "Sostenibilità"
                        },
                        {
                            type: "discount",
                            value: "-50%"
                        }
                    ]
                },
                {
                    id: 2,
                    frontImage: "2.webp",
                    backImage: "2b.webp",
                    brand: "Guess",
                    name: "Roses Tee",
                    price: 20.99,
                    isInFavorites: true,
                    badges: [
                        {
                            type: "discount",
                            value: "-30%"
                        }
                    ]
                },
                {
                    id: 3,
                    frontImage: "3.webp",
                    backImage: "3b.webp",
                    brand: "Come Zucchero Filato",
                    name: "Voglia di colori pastello",
                    price: 129.99,
                    isInFavorites: false,
                    badges: [
                        {
                            type: "discount",
                            value: "-30%"
                        }
                    ]
                },
                {
                    id: 4,
                    frontImage: "4.webp",
                    backImage: "4b.webp",
                    brand: "Levi's",
                    name: "Tee Unisex",
                    price: 14.99,
                    isInFavorites: false,
                    badges: [
                        {
                            type: "tag",
                            value: "Sostenibilità"
                        },
                        {
                            type: "discount",
                            value: "-50%"
                        }
                    ]
                },
                {
                    id: 5,
                    frontImage: "5.webp",
                    backImage: "5b.webp",
                    brand: "Maya Deluxe",
                    name: "Stripe Bodice",
                    price: 99.99,
                    isInFavorites: true,
                    badges: [
                        {
                            type: "tag",
                            value: "Sostenibilità"
                        },
                        {
                            type: "discount",
                            value: "-50%"
                        }
                    ]
                },
                {
                    id: 6,
                    frontImage: "6.webp",
                    backImage: "6b.webp",
                    brand: "Esprit",
                    name: "Maglione - Black",
                    price: 29.99,
                    isInFavorites: true,
                    badges: [
                        {
                            type: "tag",
                            value: "Sostenibilità"
                        }
                    ]
                }
            ]
        }
    }
}

</script>

<template>

    <main>
        <section>
            <div class="container">
                <div class="row">

                    <CardComponent v-for="(product, i) in products" :item="product" :key="i" />

                    <!-- <div class="col-3">
                        <div class="top-card">
                            <img src="/public/img/1.webp" alt="" class="principale">
                            <div class="badge-container">
                                <span class="badge-rosso">-50%</span>
                                <span class="badge-verde">Sostenibilità</span>
                            </div>
                            <span class="badge-cuore"> &hearts; </span>

                            <div class="over">
                                <img src="/public/img/1b.webp" alt="" class="secondaria">
                            </div>
                        </div>
                        <div class="bottom-card">
                            <p>Levi's</p>
                            <p>
                            <h4>RELAXED FIT TEE UNISEX</h4>
                            </p>
                            <p><span>14,98€</span><del>29,99€</del></p>
                        </div>
                    </div>

                    <div class="col-3">
                        <div class="top-card">
                            <img src="/public/img/2.webp" alt="" class="principale">
                            <div class="badge-container">
                                <span class="badge-rosso">-30%</span>
                            </div>
                            <span class="badge-cuore"> &hearts; </span>

                            <div class="over">
                                <img src="/public/img/2b.webp" alt="" class="secondaria">
                            </div>
                        </div>
                        <div class="bottom-card">
                            <p>Guess</p>
                            <p>
                            <h4>ROSES TEE</h4>
                            </p>
                            <p><span>20,99€</span><del>29,99€</del></p>
                        </div>
                    </div>

                    <div class="col-3">
                        <div class="top-card">
                            <img src="/public/img/3.webp" alt="" class="principale">
                            <div class="badge-container">
                                <span class="badge-rosso">-30%</span>
                            </div>
                            <span class="badge-cuore"> &hearts; </span>

                            <div class="over">
                                <img src="/public/img/3b.webp" alt="" class="secondaria">
                            </div>
                        </div>
                        <div class="bottom-card">
                            <p>Come Zucchero Filato</p>
                            <p>
                            <h4>VOGLIA DI COLORI PASTELLO</h4>
                            </p>
                            <p><span>129,99€</span><del>184,99€</del></p>
                        </div>
                    </div>

                    <div class="col-3">
                        <div class="top-card">
                            <img src="/public/img/4.webp" alt="" class="principale">
                            <div class="badge-container">
                                <span class="badge-rosso">-50%</span>
                                <span class="badge-verde">Sostenibilità</span>
                            </div>
                            <span class="badge-cuore"> &hearts; </span>

                            <div class="over">
                                <img src="/public/img/4b.webp" alt="" class="secondaria">
                            </div>
                        </div>
                        <div class="bottom-card">
                            <p>Levi's</p>
                            <p>
                            <h4>TEE UNISEX</h4>
                            </p>
                            <p><span>14,98€</span><del>29,99€</del></p>
                        </div>
                    </div>

                    <div class="col-3">
                        <div class="top-card">
                            <img src="/public/img/5.webp" alt="" class="principale">
                            <span class="badge-cuore"> &hearts; </span>

                            <div class="over">
                                <img src="/public/img/5b.webp" alt="" class="secondaria">
                            </div>
                        </div>
                        <div class="bottom-card">
                            <p>Maya Deluxe</p>
                            <p>
                            <h4>STRIPE BODICE</h4>
                            </p>
                            <p><span>99,99€</span></p>
                        </div>
                    </div>

                    <div class="col-3">
                        <div class="top-card">
                            <img src="/public/img/6.webp" alt="" class="principale">
                            <div class="badge-container">
                                <span class="badge-verde">Sostenibilità</span>
                            </div>
                            <span class="badge-cuore"> &hearts; </span>

                            <div class="over">
                                <img src="/public/img/6b.webp" alt="" class="secondaria">
                            </div>
                        </div>
                        <div class="bottom-card">
                            <p>Esprit</p>
                            <p>
                            <h4>MAGLIONE BLACK</h4>
                            </p>
                            <p><span>29,99€</span></p>
                        </div>
                    </div> -->
                </div>
            </div>
        </section>
    </main>

</template>

<style lang="scss" scoped>
@use './styleNew/general'
</style>