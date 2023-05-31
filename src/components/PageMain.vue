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
                        px: 0
                    },
                    {
                        text: '"FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES"',
                        color: "black",
                        fs: 1.5,
                        mb: .5,
                        px: 35
                    },
                    {
                        text: 'WASHINGTON POST 2018',
                        color: "#b7903c",
                        fs: .8,
                        mb: 0,
                        px: 0
                    }
                ],
                [
                    {
                        text: '"',
                        color: "#b7903c",
                        fs: 10,
                        mb: -7,
                        px: 0
                    },
                    {
                        text: '"WOW TOP PIZZA!"',
                        color: "black",
                        fs: 1.5,
                        mb: .5,
                        px: 35
                    },
                    {
                        text: 'LORENZO POST 2022',
                        color: "#b7903c",
                        fs: .8,
                        mb: 0,
                        px: 0
                    }
                ],
                [
                    {
                        text: '"',
                        color: "#b7903c",
                        fs: 10,
                        mb: -7,
                        px: 0
                    },
                    {
                        text: '"TASTE MLMLML"',
                        color: "black",
                        fs: 1.5,
                        mb: .5,
                        px: 35
                    },
                    {
                        text: 'FABRIZIO POST 2019',
                        color: "#b7903c",
                        fs: .8,
                        mb: 0,
                        px: 0
                    }
                ]
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
        <SliderCarousel :offsetY="2" :dotPosition="false" style="height: 620px;" :bgAnimationDuration="50" bgImage="../src/assets/img/cielostellato.PNG"
            :imagesList="jumboImages" :imagesWidth="[35, 13]" :autoplay="true" :autoplayDelay="4" :animationDuration="1" />
        <div class="d-flex gap-2">
            <div v-for="CardViewMoreData in CardViewMoreDataList" class="flex-fill">
                <CardViewMore :imgPath="CardViewMoreData" />
            </div>
        </div>
        <div class="my-reviewBg">
            <SliderCarousel :offsetY="-3" :dotPosition="true" style="height: 400px;" :textList="reviewSliderTextList" :autoplay="false" :autoplayDelay="4"
                :animationDuration="1" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
.my-reviewBg {
    background-image: url("../src/assets/img/h3-testimonials-bckgrnd.jpg");
    background-size: contain;
}
</style>
