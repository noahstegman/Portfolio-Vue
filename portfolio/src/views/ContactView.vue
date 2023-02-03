<script setup>

import navView from '../components/nav.vue';
import footerView from '../components/footer.vue'

</script>

<template>
    <navView :notHome="true"/>
    <div class="link-wrapper">
        <a href="/pdf/StegmanNoahResume.pdf"><div class="resume">Resume.PDF</div></a>
        <div class="email">stegmannoah@gmail.com</div>
    </div>
    <footerView />
</template>


<style scoped>

.link-wrapper{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
}

.link-wrapper > div, a{
    font-family: 'IBM Plex Mono', monospace;
    font-weight: 300;
    font-size: calc(2vw + 10px);
    text-decoration: none;
}

a{
    color: rgb(39, 39, 191);
}

a:hover{
    border-bottom: 1px solid rgb(39, 39, 191);
}

</style>