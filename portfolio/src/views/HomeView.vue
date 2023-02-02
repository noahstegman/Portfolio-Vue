<script setup>
import navView from '../components/nav.vue';
import footerView from '../components/footer.vue'
import linksView from '../components/links.vue'
import links from "../data/data.json"
import {RouterLink} from "vue-router"


</script>

<template>
    <navView />
    <div class="link-wrapper">
        <RouterLink v-for="link in links" :to="`/${link.id}`"><linksView :naming="link.id"/></RouterLink>    
    </div>
    <footerView />
</template>

<style scoped>
    .link-wrapper{
        height: calc(100% - 225px);
        width: 100%;
        background-color: rgba(255, 255, 255, 0.1);
        display: flex;
        flex-wrap: wrap;
    }
    a{
        width: calc(50% - 2px);
        height: calc(50% - 2px);
        transition: all .2 linear;
        border: 1px #222 solid;
        text-decoration: none;
    }
    a:hover{
        background-color: rgba(0, 0, 0, 0.15);
        transition: all .1s linear;
    }

</style>