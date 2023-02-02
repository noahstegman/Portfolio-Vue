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
                    <img class="p-img" :src="project.img"/>
                    <p>{{ project.name }}</p>
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

.projectlist{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    padding-bottom: 60px;
    height: fit-content;
}

h1{
    font-family: 'Open Sans', sans-serif;
    font-size: 50px;
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
    height: 250px;
    margin: 25px;
    border-radius: 25px;
    background-color: rgba(0, 0, 0, 0.2);
}
p{
    font-family: 'Open Sans', sans-serif;
    font-size: 30px;
    margin: 0px;
}

</style>