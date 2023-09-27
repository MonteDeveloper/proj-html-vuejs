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
                    "../assets/img/h3-rev-img-1.png",
                    "../assets/img/h3-rev-img-2.png"
                ],
                [
                    "../assets/img/h3-rev-img-3.png",
                    "../assets/img/h3-rev-img-4.png"
                ],
                [
                    "../assets/img/h3-rev-img-5.png",
                    "../assets/img/h3-rev-img-6.png"
                ]
            ],
            cardViewMoreDataList: [
                "../assets/img/h3-img-1.jpg",
                "../assets/img/h3-img-2.jpg",
                "../assets/img/h3-img-3.jpg",
                "../assets/img/h3-img-4.jpg"
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
            delishPizzaListText: [
                {
                    pointText: ["02", "NOV"],
                    title: "TRADITIONAL NAPOLITAN PIES IN KYOTO PIZZA MERCATO",
                    position: "204 E. Pizzetta Tommaso"
                },
                {
                    pointText: ["03", "NOV"],
                    title: "TERARAZZA PATIO DINING SPACE OPENING THIS WEEKEND",
                    position: "204 E. Pizzetta Tommaso"
                },
                {
                    pointText: ["05", "NOV"],
                    title: "SIENNA PRIVATE DINING ROOM WITH STEPHANE BRUNN",
                    position: "204 E. Pizzetta Tommaso"
                }
            ],
            cardPersonDataList: [
                {
                    imgPath: "../assets/img/h1-team-1a-700x700.jpg",
                    name: "JANE SMITH",
                    description: "Pizza Chef"
                },
                {
                    imgPath: "../assets/img/h1-team-2a.jpg",
                    name: "SARAH JOHNSON",
                    description: "Dough Maker"
                },
                {
                    imgPath: "../assets/img/h1-team-4a.jpg",
                    name: "FANK BALEY",
                    description: "Kitchen Porter"
                },
                {
                    imgPath: "../assets/img/h1-team-3a.jpg",
                    name: "EMILY JONES",
                    description: "Waitress"
                }
            ],
            partnerLogoDataList: [
                "../assets/img/h1-clients-img-1.png",
                "../assets/img/h1-clients-img-2.png",
                "../assets/img/h1-clients-img-3.png",
                "../assets/img/h1-clients-img-4.png",
                "../assets/img/h1-clients-img-5.png",
            ],
            cardPizzaData: {
                imgPathList: [
                    "../assets/img/h3-product-img-1a-100x100.png",
                    "../assets/img/h3-product-img-2a-150x150.png",
                    "../assets/img/h3-product-img-3a-150x150.png",
                    "../assets/img/h3-product-img-4a-150x150.png",
                    "../assets/img/h3-product-img-5a-150x150.png",
                    "../assets/img/h3-product-img-6a-100x100.png",
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
                bgImage="../assets/img/cielostellato.PNG" :imagesList="jumboImages" :imagesWidth="[35, 13]"
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
            <CardListBar class="pb-5" :imgPathList="cardPizzaData.imgPathList" :textList="cardPizzaData.textList"
                :isAnimated="true" :cardImgPx="2" />
        </section>

        <!-- DELISH PIZZA DEALS DATES -->
        <section>
            <div class="d-flex flex-wrap">
                <div class="my-bgStars col-12 col-md-6 p-5 text-white d-flex justify-content-center align-items-center">
                    <div class="my-maxWidth">
                        <p class="text-danger m-0">MADE WITH LOVE</p>
                        <h2 class="h1 mb-5">DELISH PIZZA DEALS</h2>
                        <ul class="list-unstyled">
                            <li v-for="delishPizzaText in delishPizzaListText" class="mb-3">
                                <div class="d-flex gap-4">
                                    <div class="text-center">
                                        <p class="text-danger h1 m-0">{{ delishPizzaText.pointText[0] }}</p>
                                        <p class="fs-5 m-0">{{ delishPizzaText.pointText[1] }}</p>
                                    </div>
                                    <div>
                                        <p class="fs-4 m-0">{{ delishPizzaText.title }}</p>
                                        <p class="text-danger m-0">{{ delishPizzaText.position }}</p>
                                    </div>
                                </div>
                                <hr class="my-hr mt-4">
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-12 col-md-6 overflow-hidden">
                    <img class="object-fit-cover" src="../assets/img/h3-img-5a.jpg" alt="">
                </div>
            </div>
        </section>

        <!-- FORM BOOK TABLE -->
        <section>
            <div class="my-form py-5 text-white">
                <div class="my-container d-flex flex-wrap justify-content-center align-items-center gap-3 my-5">
                    <select class="text-secondary" name="personNumber" id="personNumberSelect">
                        <option v-for="i in 10" value="i">{{ i }} Person{{i > 1 ? 's' : ''}}</option>
                    </select>
                    <span>FOR</span>
                    <input class="text-secondary" type="date" name="dateInput" id="dateInput">
                    <span>AT</span>
                    <input class="text-secondary" type="time" name="timeInput" id="timeInput">
                    <button class="my-orangeBtn">BOOK A TABLE</button>
                </div>
            </div>
        </section>
    </div>
</template>

<style lang="scss" scoped>
.my-form {
    background-image: url("../assets/img/h3-background-img-3.jpg");
    background-size: cover;

    input,
    select {
        padding: .5rem 2rem;
        text-align: start;
        border: 1px solid black;
    }

    button,
    input,
    select{
        width: 200px;
        height: 50px;
    }

    select {
        -webkit-appearance: none;
        -moz-appearance: none;
        appearance: none;
        background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24"><path fill="%23bd994f" d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/></svg>');
        background-repeat: no-repeat;
        background-position: right .5rem center;
        background-size: 1em;
    }

    #dateInput::-webkit-calendar-picker-indicator {
        background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 24 24"><path fill="%23bd994f" d="M20 3h-1V1h-2v2H7V1H5v2H4c-1.1 0-2 .9-2 2v16c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm0 18H4V8h16v13z"/></svg>');
        background-repeat: no-repeat;
    }

    #timeInput::-webkit-calendar-picker-indicator {
        background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24"><path fill="%23bd994f" d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm4.25 13.46l-4.24-4.24V7h1.5v3.67l3.74 3.74-1.06 1.06z" /> </svg> ');
    }
}

.my-hr {
    border: 1px dotted #b7903c;
}

.my-darkerWhiteBg {
    background-color: #f7f7f2;
}

.my-reviewBg {
    background-image: url("../assets/img/h3-testimonials-bckgrnd.jpg");
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
