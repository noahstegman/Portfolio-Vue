<script setup>

import navView from '../components/nav.vue';
import footerView from '../components/footer.vue'
import links from '../data/links.json'

</script>

<template>
    <navView :notHome="true"/>
    <div class="link-wrapper">
        <div class="links-wrapper">
            <div v-for="url, site in links" class="links">
                <span class="sitename">{{ site }}</span>
                <a :href="url"><span>{{ url }}</span></a>
            </div>
        </div>
    </div>
    <footerView />
</template>

<style scoped>

.links-wrapper{
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.links{
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100vw;
    font-family: 'IBM Plex Mono', monospace;
    font-weight: 300;
    font-size: calc(2vw + 10px);
    height: 100px;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}

@media screen and (max-width: 1700px) {
    .sitename{
        display: none;
    }
    .links{
        justify-content: center;
    }
}
span{
    
    padding-left: 50px;
    padding-right: 50px;
}

</style>