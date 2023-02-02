<script setup>
import navView from '../components/nav.vue';
import footerView from '../components/footer.vue'
import linksView from '../components/links.vue'
import links from "../data/data.json"
import {RouterLink} from "vue-router"


</script>

<template>
    <navView :nothome="false"/>
    <div class="link-wrapper">
        <RouterLink v-for="link in links" :to="`/${link.id}`" class="arl"><linksView :naming="link.id"/></RouterLink>    
    </div>
    <footerView />
</template>

<style scoped>

</style>