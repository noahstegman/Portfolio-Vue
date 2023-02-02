<script setup>

import navView from '../components/nav.vue';
import footerView from '../components/footer.vue';
import about from '../data/about.json';

</script>

<template>
    <navView :notHome="true"/>
    <div class="link-wrapper">  
        <div class="about-wrapper">
            <div class="img"><img v-bind:src="about['img-url']"/></div>
            <div class="text">
                <p v-for="paragraph in about.text">
                    {{ paragraph }}
                </p>
            </div>
        </div>
    </div>
    <footerView />
</template>


<style scoped>

.about-wrapper{
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
}
.img{
    padding: 15px;
}

img{
    height: auto;
    border-radius: 15px;
    width: calc(15vw + 200px);
}

.text{
    padding-top: 25px;
    font-family: 'Open Sans', sans-serif;
    font-size: 22px;
    max-width: 600px;
}

@media screen and (min-width: 716px) {
    .about-wrapper{
        flex-direction: row;
    }
    img{
    height: auto;
    border-radius: 15px;
    width: calc(15vw + 200px);
    }
}   
@media screen and (max-width: 716px) {
    .about-wrapper{
        flex-direction: column;
        height: fit-content;
    }
    img{
    height: auto;
    border-radius: 15px;
    width: 80vw;
    max-width: 400px;
    }
}

</style>