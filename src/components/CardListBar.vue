<script>

export default {
    name: "CardListBar",
    props: {
        imgPathList: Array,
        textList: Array,
        isAnimated: Boolean,
        cardImgPx: Number
    },
    data() {
        return {
            animateNumberLoop: 0
        }
    },
    mounted() {
        this.isAnimated ? this.animateNumberLoop = 2 : this.animateNumberLoop = 1;
        if(this.textList){
            console.log(this.textList[0].cardText)
        }
        // console.log("Caricato il componente 'CardListBar'.");
    }
}
</script>

<template>
    <div class="overflow-hidden">
        <div :class="{'my-animatedBar': isAnimated}">
            <div class="d-flex" :style="`width: ${isAnimated ? 110 : 100}%`" >
                <div class="d-flex w-100" v-for="i in animateNumberLoop">
                    <div class="d-flex flex-column" v-for="(imgPath, index) in imgPathList" :style="`width: ${100 / imgPathList.length}%;`">
                        
                        <img class="img-fluid" :src="imgPath" alt="imgInBar" :style="`padding: 0 ${cardImgPx}rem;`">
                        
                        <div class="p-3 text-center" v-if="textList && textList[index]">
                            <p class="m-0" v-for="rowText in textList[index].cardText">
                                <span v-for="text in rowText" >
                                    <span :class="text.classList">{{text.text }}</span>
                                    <span v-if="rowText.length > 1">{{ ' ' }}</span>
                                </span>
                                <br>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@keyframes scroll {
  from { transform: translateX(0); }
  to { transform: translateX(-55%); }
}

.my-animatedBar{
    width: 200%;
    animation: scroll linear infinite 25s;
}
</style>
