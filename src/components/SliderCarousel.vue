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
        bgAnimationDuration: Number
    },
    data() {
        return {
            currentIndex: 0,
            animationName: 'slide-left',
            isAnimating: false,
            autoSlider: undefined
        }
    },
    methods: {
        next() {
            if (!this.isAnimating) {
                this.isAnimating = true;
                this.animationName = 'slide-left';
                this.currentIndex =
                    this.currentIndex === this.imagesList.length - 1
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
                        ? this.imagesList.length - 1
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

        <div class="my-bgSlider d-flex" :style="`animation-duration: ${bgAnimationDuration}s`">
            <img :src="bgImage" alt="background_slider">
            <img :src="bgImage" alt="background_slider">
        </div>

        <transition-group :name="animationName" tag="div" class="my-carousel">
            <div v-for="(images, index) in imagesList" :key="index" v-show="index === currentIndex"
                class="my-carousel-item h-100 w-100" @animationend="isAnimating = false"
                :style="`animation-duration: ${animationDuration}s`">

                <img class="mt-5" v-for="(image, i) in images" :src="image" :style="`width: ${imagesWidth[i]}%; animation-duration: ${animationDuration}s;`" />

            </div>
        </transition-group>
    </div>
</template>

<style lang="scss" scoped>
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

    &:hover {
        transform: translate(0%, 55%);
    }
}

.my-rotateLeft {
    rotate: 90deg;
    transform: translate(0%, 50%);
}

.my-rotateRight {
    rotate: -90deg;
    transform: translate(0%, 50%);
}

.my-carousel {
    position: relative;
    width: 100%;
    // background-image: url("../src/assets/img/cielostellato.PNG");
    // background-size: cover;
    // background-position: bottom;
    height: 620px;
    overflow: hidden;
}

@keyframes scroll {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}

.my-bgSlider{
    position: absolute;
    top: 0;
    left: 0%;
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

.my-carousel-item img {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

@keyframes slideRight {
    0% {
        transform: translate(150%, -50%);
    }

    100% {
        transform: translate(-50%, -50%);
    }
}

@keyframes slideLeft {
    0% {
        transform: translate(-150%, -50%);
    }

    100% {
        transform: translate(-50%, -50%);
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
  