<script>
import SliderCarousel from './SliderCarousel.vue'
import CardViewMore from './CardViewMore.vue'
import CardPerson from './CardPerson.vue'
import CardListBar from './CardListBar.vue'

export default {
    name: "PageMain",
    components: {
        SliderCarousel,
        CardViewMore,
        CardPerson,
        CardListBar
    },
    data() {
        return {
            jumboImages: [
                [
                    "../src/assets/img/h3-rev-img-1.png",
                    "../src/assets/img/h3-rev-img-2.png"
                ],
                [
                    "../src/assets/img/h3-rev-img-3.png",
                    "../src/assets/img/h3-rev-img-4.png"
                ],
                [
                    "../src/assets/img/h3-rev-img-5.png",
                    "../src/assets/img/h3-rev-img-6.png"
                ]
            ],
            cardViewMoreDataList: [
                "../src/assets/img/h3-img-1.jpg",
                "../src/assets/img/h3-img-2.jpg",
                "../src/assets/img/h3-img-3.jpg",
                "../src/assets/img/h3-img-4.jpg"
            ],
            reviewSliderTextList: [
                [
                    {
                        text: '"',
                        color: "#b7903c",
                        fs: 10,
                        mb: -7,
                        maxWidth: 800
                    },
                    {
                        text: '"FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES"',
                        color: "black",
                        fs: 1.5,
                        mb: .5,
                        maxWidth: 800
                    },
                    {
                        text: 'WASHINGTON POST 2018',
                        color: "#b7903c",
                        fs: .8,
                        mb: 0,
                        maxWidth: 800
                    }
                ],
                [
                    {
                        text: '"',
                        color: "#b7903c",
                        fs: 10,
                        mb: -7,
                        maxWidth: 800
                    },
                    {
                        text: '“THIS PIZZERIA IN NAPLES IS A HIDDEN GEM! THEIR NEW YORK-STYLE PIZZA SLICES ARE THE BEST IN TOWN.”',
                        color: "black",
                        fs: 1.5,
                        mb: .5,
                        maxWidth: 800
                    },
                    {
                        text: 'THE GUARDIAN 2019',
                        color: "#b7903c",
                        fs: .8,
                        mb: 0,
                        maxWidth: 800
                    }
                ],
                [
                    {
                        text: '"',
                        color: "#b7903c",
                        fs: 10,
                        mb: -7,
                        maxWidth: 800
                    },
                    {
                        text: '“DON’T MISS OUT ON THIS PIZZERIA IN NAPLES. THEIR NEW YORK-STYLE PIZZA SLICES ARE UNBEATABLE.”',
                        color: "black",
                        fs: 1.5,
                        mb: .5,
                        maxWidth: 800
                    },
                    {
                        text: 'THE NEW YORK TIMES 2020',
                        color: "#b7903c",
                        fs: .8,
                        mb: 0,
                        maxWidth: 800
                    }
                ],
                [
                    {
                        text: '"',
                        color: "#b7903c",
                        fs: 10,
                        mb: -7,
                        maxWidth: 800
                    },
                    {
                        text: '“IF YOU’RE LOOKING FOR THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES, LOOK NO FURTHER THAN THIS PIZZERIA. IT’S A MUST-VISIT!”',
                        color: "black",
                        fs: 1.5,
                        mb: .5,
                        maxWidth: 800
                    },
                    {
                        text: 'TIME OUT 2021',
                        color: "#b7903c",
                        fs: .8,
                        mb: 0,
                        maxWidth: 800
                    }
                ]
            ],
            specialListText: [
                {
                    pointText: "$10",
                    title: "COMBO PICCOLO",
                    description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Incidunt iusto facere, eveniet temporibus."
                },
                {
                    pointText: "$20",
                    title: "COMBO MEZZO",
                    description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Incidunt iusto facere, eveniet temporibus."
                },
                {
                    pointText: "$30",
                    title: "COMBO GRANDE",
                    description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Incidunt iusto facere, eveniet temporibus."
                }
            ],
            cardPersonDataList: [
                {
                    imgPath: "../src/assets/img/h1-team-1a-700x700.jpg",
                    name: "JANE SMITH",
                    description: "Pizza Chef"
                },
                {
                    imgPath: "../src/assets/img/h1-team-2a.jpg",
                    name: "SARAH JOHNSON",
                    description: "Dough Maker"
                },
                {
                    imgPath: "../src/assets/img/h1-team-4a.jpg",
                    name: "FANK BALEY",
                    description: "Kitchen Porter"
                },
                {
                    imgPath: "../src/assets/img/h1-team-3a.jpg",
                    name: "EMILY JONES",
                    description: "Waitress"
                }
            ],
            partnerLogoDataList: [
                "../src/assets/img/h1-clients-img-1.png",
                "../src/assets/img/h1-clients-img-2.png",
                "../src/assets/img/h1-clients-img-3.png",
                "../src/assets/img/h1-clients-img-4.png",
                "../src/assets/img/h1-clients-img-5.png",
            ],
            cardPizzaData: {
                imgPathList: [
                    "../src/assets/img/h3-product-img-1a-100x100.png",
                    "../src/assets/img/h3-product-img-2a-150x150.png",
                    "../src/assets/img/h3-product-img-3a-150x150.png",
                    "../src/assets/img/h3-product-img-4a-150x150.png",
                    "../src/assets/img/h3-product-img-5a-150x150.png",
                    "../src/assets/img/h3-product-img-6a-100x100.png",
                ],
                textList: [
                    {
                        circleText: "SOLD",
                        cardText: [
                            [
                                {
                                    text: "BISMARK",
                                    classList: "my-pizzaCardTitle"
                                }
                            ],
                            [
                                {
                                    text: "$25.00",
                                    classList: "my-discountPriceText"
                                },
                                {
                                    text: "$30.00",
                                    classList: "my-priceText"
                                }
                            ]
                        ]
                    },
                    {
                        circleText: "",
                        cardText: [
                            [
                                {
                                    text: "FIORI DI ZUCCA",
                                    classList: "my-pizzaCardTitle"
                                }
                            ],
                            [
                                {
                                    text: "$7.00 - $50.00",
                                    classList: "my-priceText"
                                }
                            ]
                        ]
                    },
                    {
                        circleText: "",
                        cardText: [
                            [
                                {
                                    text: "VALDOSTANA",
                                    classList: "my-pizzaCardTitle"
                                }
                            ],
                            [
                                {
                                    text: "$55.00",
                                    classList: "my-priceText"
                                }
                            ]
                        ]
                    },
                    {
                        circleText: "",
                        cardText: [
                            [
                                {
                                    text: "PIZZA TARTUFATA",
                                    classList: "my-pizzaCardTitle"
                                }
                            ],
                            [
                                {
                                    text: "$45.00",
                                    classList: "my-priceText"
                                }
                            ]
                        ]
                    },
                    {
                        circleText: "",
                        cardText: [
                            [
                                {
                                    text: "FRANCESCANA",
                                    classList: "my-pizzaCardTitle"
                                }
                            ],
                            [
                                {
                                    text: "$25.00",
                                    classList: "my-priceText"
                                }
                            ]
                        ]
                    },
                    {
                        circleText: "",
                        cardText: [
                            [
                                {
                                    text: "CAMPAGNOLA",
                                    classList: "my-pizzaCardTitle"
                                }
                            ],
                            [
                                {
                                    text: "$50.00 - $95.00",
                                    classList: "my-priceText"
                                }
                            ]
                        ]
                    }
                ]
            }
        }
    },
    mounted() {
        console.log("Caricato il componente 'PageMain'.");
    }
}
</script>

<template>
    <div class="d-flex flex-column gap-2">
        <!-- JUMBO -->
        <section>
            <SliderCarousel :offsetY="2" :dotPosition="false" style="height: 620px;" :bgAnimationDuration="50"
                bgImage="../src/assets/img/cielostellato.PNG" :imagesList="jumboImages" :imagesWidth="[35, 13]"
                :autoplay="true" :autoplayDelay="4" :animationDuration="1" />
        </section>

        <!-- CARD VIEWMORE -->
        <section>
            <div class="d-flex gap-2">
                <div v-for="cardViewMoreData in cardViewMoreDataList" class="flex-fill">
                    <CardViewMore :imgPath="cardViewMoreData" />
                </div>
            </div>
        </section>

        <!-- REVIEWS -->
        <section>
            <div class="my-reviewBg">
                <SliderCarousel :offsetY="-3" :dotPosition="true" style="height: 500px;" :textList="reviewSliderTextList"
                    :autoplay="false" :autoplayDelay="4" :animationDuration="1" />
            </div>
        </section>

        <!-- SPECIALS* LIST -->
        <section>
            <div class="d-flex flex-wrap">
                <div class="col-12 col-lg-6 position-relative overflow-hidden">
                    <img class="h-100 w-100" src="../assets/img/h1-img-4.jpg" alt="bgImg-1">
                    <img class="col-5 position-absolute start-50 top-50 translate-middle" src="../assets/img/h1-img-7n.png"
                        alt="bgImg-1">
                </div>
                <div class="col-12 col-lg-6 d-flex justify-content-center align-items-center py-5">
                    <div class="col-lg-10 col-xxl-6">
                        <h2 class="h1">SPECIALS*</h2>
                        <p class="text-secondary">
                            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Incidunt iusto facere, eveniet
                            temporibus.
                        </p>
                        <ul class="list-unstyled">
                            <li v-for="specialText in specialListText" class="mb-3">
                                <div class="d-flex gap-2">
                                    <div>
                                        <span class="text-danger fs-4">{{ specialText.pointText }}</span>
                                    </div>
                                    <div>
                                        <span class="fs-4">{{ specialText.title }}</span> <br>
                                        <span class="text-secondary">{{ specialText.description }}</span>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- BANNER GO AHED -->
        <section>
            <div class="my-goAhedBg bg-danger">
                <div class="my-container d-flex align-items-center h-100">
                    <p class="h1 text-white">
                        GO AHED AND <br>
                        BUILD YOUR <br>
                        OWN PIZZA <br>
                        WE WON'T <br>
                        JUDGE!
                    </p>
                </div>
            </div>
        </section>

        <!-- CARD PERSON -->
        <section>
            <div class="d-flex">
                <div v-for="cardPersonData in cardPersonDataList" class="col-3">
                    <CardPerson :imgPath="cardPersonData.imgPath" :name="cardPersonData.name"
                        :description="cardPersonData.description" :cardBackColor="'#d2401e'" />
                </div>
            </div>
        </section>

        <!-- LOGO PARTNER LIST -->
        <section class="my-darkerWhiteBg py-5">
            <div class="my-container">
                <CardListBar :imgPathList="partnerLogoDataList" :isAnimated="false" />
            </div>
        </section>

        <!-- PIZZA MENU LIST -->
        <section>
            <div class="d-flex justify-content-center">
                <div class="text-center px-2 py-5 my-maxWidth">
                    <p class="text-danger">CHOOSE YOUR FLAVOR</p>
                    <h2 class="h1">THE BEST PIZZA MENU IN TOWN</h2>
                    <p class="text-secondary">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Inventore, autem asperiores odio earum
                        sequi quam nisi repellendus id accusantium! Repudiandae, id atque.
                    </p>
                </div>
            </div>
            <CardListBar :imgPathList="cardPizzaData.imgPathList" :textList="cardPizzaData.textList" :isAnimated="true" :cardImgPx="2"/>
        </section>
    </div>
</template>

<style lang="scss" scoped>

.my-darkerWhiteBg{
    background-color: #f7f7f2;
}
.my-reviewBg {
    background-image: url("../src/assets/img/h3-testimonials-bckgrnd.jpg");
    background-size: contain;
}

.my-maxWidth {
    max-width: 700px;
}

.my-goAhedBg {
    height: 450px;
    background-image: url(../assets/img/h3-background-img-duplicated.jpg);
    background-size: 150%;
    background-position: center;
    background-attachment: fixed;

    .my-container {

        padding: 0 10rem;
    }
}
</style>
