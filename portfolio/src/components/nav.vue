<script setup>
    import {ref} from "vue";
    import links from "../data/data.json";
    import { RouterLink } from "vue-router";

    const props = defineProps(['notHome'])

    const message = ["noah stegman"]
    const speed = 140
    let textPosition = 0;
    function typewriter() {
        document.querySelector("#message").innerHTML = message[0].substring(0, textPosition) + '<span id="blinky">|</span>'
        if(textPosition++ != message[0].length)
            setTimeout(typewriter, speed)
        }



    window.addEventListener("load", typewriter);
</script>

<template>
    <div class="navigation">
        <div id="message" >noah stegman</div>
        <div class="nonnav-wrapper" v-show="props.notHome">
            <RouterLink v-for="link in links" :to="`/${link.id}`" class="nonnav">
                {{ link.id }}
            </RouterLink>
        </div>
    </div>
</template>

<style scoped>
    .navigation{
        border-bottom: 1px solid #222;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: rgba(0, 0, 0, 0.02);
        height: 174px;
        flex-direction: column;
        font-family: 'IBM Plex Mono', monospace;
        font-weight: 300;
        font-size: calc(2vw + 35px)
    }
    .nonnav{
        font-size: 30px;
    }
    .nonnav-wrapper{
        display: flex;
        justify-content: space-evenly;
        height: 100px;
        width: 100%;
        align-items: center
    }


</style>