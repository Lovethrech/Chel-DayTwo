<style scoped>
.landing-page-nav-mini-ctn{
    position:fixed;
    z-index:10;
    width:50%;
    height:70%;
    background-color:rgba(96, 110, 148, 0.342);
    backdrop-filter: blur(10px) saturate(180%);
    border: 10px inset rgba(96, 110, 148, 0.302);
    box-shadow: 2px 2px 10px 2px rgba(0, 0, 0, 0.904);
}

@media screen and (max-width:950px) {
    .landing-page-nav-mini-ctn{
        width:90%;
        height:80vh;
    }
}
</style>
<template>
    <div class="landing-page-nav-mini-ctn"></div>
</template>