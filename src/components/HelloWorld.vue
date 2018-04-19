<template>
    <div class="hello">
        <div class="circles">
            <div v-for="(n) in 10" :key="'circle'+n" @click="moveCricle" class="circle"></div>
        </div>
    </div>
</template>

<script>
    import {TweenMax} from 'gsap';

    export default {
        name: 'HelloWorld',
        methods: {
            moveCricle() {
                TweenMax.staggerFromTo(".circle", 1, {
                    x: 0,
                }, {
                    x: 100,
                    ease: Elastic.easeOut
                }, 1)
            }
        },
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .circle {
        width: 20px;
        height: 20px;
        border-radius: 50%;
        background: black;
        margin-top: 20px;
        display: block;
        margin-left: auto;
        margin-right: auto;
    }
</style>
