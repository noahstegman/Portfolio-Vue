<script setup>

import navView from '../components/nav.vue';
import footerView from '../components/footer.vue'
import projects from '../data/projects.json'


</script>

<template>
    <navView :notHome="true"/>
    <div class="link-wrapper"> 
        <div class="project-wrapper">
            <div class="text"><h1>Projects</h1></div>
            <div class="projectlist">
                <div v-for="project in projects" class="project">
                    <a :href="project.url">
                    <img class="p-img" :src="project.img"/>
                    <p>{{ project.name }}</p>
                    <p class="info">{{ project.description }}</p>
                    </a>
                </div>
            </div>
        </div>
    </div>
    <footerView />
</template>

<style scoped>

.project-wrapper{
  display: flex;
  text-align: center;
  flex-direction: column;
  height: 100%;
  width: 100%;
}

.info{
    font-size: 20px;
    text-align: justify;
    padding: 20px;
}

.projectlist{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    align-items: flex-start;
    padding-bottom: 60px;
    height: fit-content;
}

h1{
    font-family: 'Open Sans', sans-serif;
    font-size: 50px;
    margin: 2px;
    font-weight: 100;
}

.p-img{
    width: 100%;
    object-fit: cover;
    height: 200px;
    border-radius: 25px 25px 0px 0px ;
}

.project{
    width: 330px;
    box-shadow: 0 3px 15px rgb(0 0 0 / 0.2);
    height: fit-content;
    margin: 25px;
    transition: .2s all linear;
    border-radius: 25px;
    background-color: rgba(0, 0, 0, 0.2);
}

.project:hover{
    transform: scale(1.2);
    -webkit-transform:scale(1.2);
    transition: .1s all linear;
}

p{
    font-family: 'Open Sans', sans-serif;
    font-size: 30px;
    margin: 0px;
}

a{
    text-decoration: none;
    color: black;
}

</style>