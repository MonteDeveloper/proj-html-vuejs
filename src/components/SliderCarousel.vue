<script>
export default {
    name: "SliderCarousel",
    props: {
        imagesList: Array,
        imagesWidth: Array,
        autoplayDelay: Number,
        animationDuration: Number,
        autoplay: Boolean,
        bgImage: String,
        bgAnimationDuration: Number,
        offsetY: Number,
        textList: Array,
        dotPosition: Boolean,
        offsetY: Number
    },
    data() {
        return {
            currentIndex: 0,
            animationName: 'slide-left',
            isAnimating: false,
            autoSlider: undefined,
            list: []
        }
    },
    methods: {
        next() {
            if (!this.isAnimating) {
                this.isAnimating = true;
                this.animationName = 'slide-left';
                this.currentIndex =
                    this.currentIndex === this.list.length - 1
                        ? 0
                        : this.currentIndex + 1;
            }
        },
        prev() {
            if (!this.isAnimating) {
                this.isAnimating = true;
                this.animationName = 'slide-right';
                this.currentIndex =
                    this.currentIndex === 0
                        ? this.list.length - 1
                        : this.currentIndex - 1;
            }
        },
        startAutoSlider() {
            if(this.autoplay && this.autoplayDelay){
                this.autoSlider = setInterval(() => {
                    this.next();
                }, 1000 * this.autoplayDelay);
            }
        },
        stopAutoSlider() {
            clearInterval(this.autoSlider);
        },
        resetAutoSlider(){
            this.stopAutoSlider();
            this.startAutoSlider();
        }
    },
    mounted() {
        if(this.imagesList){
            this.list = this.imagesList;
        }else if(this.textList){
            this.list = this.textList;
        }
        console.log(this.list);
        this.startAutoSlider();
    }
}
</script>

<template>
    <div class="position-relative overflow-hidden">
        <button class="my-rotateLeft position-absolute top-50 start-0" @click="prev(); resetAutoSlider()">
            <strong>PREV</strong>
        </button>
        <button class="my-rotateRight position-absolute top-50 end-0" @click="next(); resetAutoSlider()">
            <strong>NEXT</strong>
        </button>

        <div v-if="bgImage" class="my-bgSlider d-flex" :style="`animation-duration: ${bgAnimationDuration}s`">
            <img :src="bgImage" alt="background_slider">
            <img :src="bgImage" alt="background_slider">
        </div>

        <transition-group :name="animationName" tag="div" class="my-carousel h-100 position-relative">
            <div v-if="imagesList" v-for="(images, index) in imagesList" :key="`img-${index}`" v-show="index === currentIndex"
                class="my-carousel-item h-100 w-100" @animationend="isAnimating = false"
                :style="`animation-duration: ${animationDuration}s; margin-top: ${offsetY}rem`" >

                <img v-for="(image, i) in images" :src="image" :style="`width: ${imagesWidth[i]}%; animation-duration: ${animationDuration}s;`" />

            </div>
            <div v-else v-for="(textGroup, index) in textList" :key="`txt-${index}`" v-show="index === currentIndex"
                class="my-carousel-item h-100 w-100" @animationend="isAnimating = false"
                :style="`animation-duration: ${animationDuration}s`">

                <div class="d-flex justify-content-center align-items-center h-100" :style="`margin-top: ${offsetY}rem`">
                    <div class="text-center">
                        <p v-for="paragraph in textGroup" :style="`color: ${paragraph.color}; font-size: ${paragraph.fs}rem; margin-bottom: ${paragraph.mb}rem; padding: 0 ${paragraph.px}rem;`">
                            {{paragraph.text}}<br>
                        </p>
                    </div>
                </div>
            </div>
            <div v-if="dotPosition" class="d-flex gap-1 position-absolute bottom-0 start-50 translate-middle-x mb-4">
                <div v-for="(n, index) in list" class="dotPosition" :class="{active: index === currentIndex}"></div>
            </div>
        </transition-group>
    </div>
</template>

<style lang="scss" scoped>
.dotPosition{
    width: 10px;
    height: 10px;
    border-radius: 100%;
    background-color: #d2401e;
    opacity: .5;
    transition: opacity .2s;

    &.active{
        opacity: 1;
    }
}

button {
    z-index: 999;
    border-radius: 50%;
    width: 70px;
    height: 70px;
    padding-bottom: 2rem;
    color: #d2401e;
    background-color: white;
    border: none;
    transition: transform .2s;
}

.my-rotateLeft {
    rotate: 90deg;
    transform: translate(-50%, 50%);

    &:hover {
        transform: translate(-50%, 55%);
    }
}

.my-rotateRight {
    rotate: -90deg;
    transform: translate(50%, 50%);

    &:hover {
        transform: translate(50%, 55%);
    }
}

.my-carousel {
    position: relative;
    width: 100%;
    overflow: hidden;
}

@keyframes scroll {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}

.my-bgSlider{
    position: absolute;
    top: 0;
    left: 0;
    overflow: hidden;
    height: 100%;
    animation: scroll linear infinite;
    img{
        width: 100vw;
        object-position: bottom;
        object-fit: cover;
    }
}

.my-carousel-item {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

.my-carousel-item img{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

@keyframes slideRight {
    0% {
        transform: translate(150%, -50%);
        opacity: 0;
    }

    100% {
        transform: translate(-50%, -50%);
        opacity: 1;
    }
}

@keyframes slideLeft {
    0% {
        transform: translate(-150%, -50%);
        opacity: 0;
    }

    100% {
        transform: translate(-50%, -50%);
        opacity: 1;
    }
}

.slide-right-enter-active {
    animation-name: slideLeft;

    img {
        animation-name: zoomOut;
    }
}

.slide-right-leave-active {
    animation-name: slideRight;
    animation-direction: reverse;

    img {
        animation-name: zoomIn;
    }
}

.slide-left-enter-active {
    animation-name: slideRight;

    img {
        animation-name: zoomOut;
    }
}

.slide-left-leave-active {
    animation-name: slideLeft;
    animation-direction: reverse;

    img {
        animation-name: zoomIn;
    }
}


@keyframes zoomOut {
    50% {
        scale: .8;
    }

    100% {
        scale: 1;
    }
}

@keyframes zoomIn {
    0% {
        scale: 1;
    }

    50% {
        scale: .8;
    }
}</style>
  