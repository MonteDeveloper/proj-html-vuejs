<script>

export default{
    name: 'SquarePatternBackground',
    data() {
        return {
            squares: [],
        }
    },
    mounted() {
        const containerWidth = this.$el.clientWidth;
        const containerHeight = this.$el.clientHeight;
        const squareSize = 10;
        const columns = Math.ceil(containerWidth / squareSize);
        const rows = Math.ceil(containerHeight / squareSize);
        for (let i = 0; i < columns * rows; i++) {
            this.squares.push({
                id: i,
            });
        }
    }
}
</script>
        
<template>
    <div class="my-container">
        <div v-for="square in squares" :key="square.id" class="my-square"></div>
    </div>
</template>
  
  
<style scoped>
.my-container {
    position: relative;
    height: 100px;
}

.my-square {
    width: 5px;
    height: 5px;
    margin: 5px;
    background-color: orange;
    float: left;
}
</style>
  