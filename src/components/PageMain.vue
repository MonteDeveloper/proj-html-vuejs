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
        <SliderCarousel :bgAnimationDuration="50" bgImage="../src/assets/img/cielostellato.PNG" :imagesList="jumboImages" :imagesWidth="[35, 13]" :autoplay="true" :autoplayDelay="4" :animationDuration="1"/>
        <div class="d-flex gap-2">
            <div v-for="CardViewMoreData in CardViewMoreDataList" class="flex-fill">
                <CardViewMore class="w-100" :imgPath="CardViewMoreData"/>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped></style>
