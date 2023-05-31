<script>
import SliderCarousel from './SliderCarousel.vue'
import CardViewMore from './CardViewMore.vue'

export default {
    name: "PageMain",
    components: {
        SliderCarousel,
        CardViewMore
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
            CardViewMoreDataList: [
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
            ]
        }
    },
    mounted() {
        console.log("Caricato il componente 'PageMain'.");
    }
}
</script>

<template>
    <div class="d-flex flex-column gap-2">
        <SliderCarousel :offsetY="2" :dotPosition="false" style="height: 620px;" :bgAnimationDuration="50"
            bgImage="../src/assets/img/cielostellato.PNG" :imagesList="jumboImages" :imagesWidth="[35, 13]" :autoplay="true"
            :autoplayDelay="4" :animationDuration="1" />
        <div class="d-flex gap-2">
            <div v-for="CardViewMoreData in CardViewMoreDataList" class="flex-fill">
                <CardViewMore :imgPath="CardViewMoreData" />
            </div>
        </div>
        <div class="my-reviewBg">
            <SliderCarousel :offsetY="-3" :dotPosition="true" style="height: 500px;" :textList="reviewSliderTextList"
                :autoplay="false" :autoplayDelay="4" :animationDuration="1" />
        </div>
        <div class="d-flex">
            <div class="col-6 position-relative">
                <img class="img-fluid" src="../assets/img/h1-img-4.jpg" alt="bgImg-1">
                <img class="img-fluid position-absolute start-50 top-50 translate-middle" src="../assets/img/h1-img-7n.png"
                    alt="bgImg-1">
            </div>
            <div class="col-6 d-flex justify-content-center align-items-center">
                <div class="w-50">
                    <h2 class="h1">SPECIALS*</h2>
                    <p class="text-secondary">
                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Incidunt iusto facere, eveniet temporibus.
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
    </div>
</template>

<style lang="scss" scoped>
.my-reviewBg {
    background-image: url("../src/assets/img/h3-testimonials-bckgrnd.jpg");
    background-size: contain;
}
</style>
