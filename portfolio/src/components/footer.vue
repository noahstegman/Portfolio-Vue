<template>
    <div class="footer">
        <span>
            built, deployed and maintained with HTML, CSS, JavaScript, VueJS, Python, NGINX, Ubuntu
        </span>
    </div>
</template>

<style scoped>

.footer{
    border-top: 1px #222 solid;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    font-family: 'Roboto Mono', monospace;
    font-weight: 300;
}

@media screen and (min-width: 715px) {
  .footer {
    height: 49px;
  }
}

@media screen and (max-width: 716px) {
  .footer {
    display: none;
  }
}

</style>