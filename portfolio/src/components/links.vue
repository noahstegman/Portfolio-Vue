<script setup>
const props = defineProps(['naming'])
</script>

<template>
    <div class="link">
        <span>{{ naming }}</span>
    </div>
</template>

<style scoped>
    .link{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 100%;
        font-family: 'Roboto Mono', monospace;
        font-weight: 200;
        font-size: calc(2vw + 20px);
    }

    span{
        border-bottom: 1px solid black;
        color: black;
    }

</style>

