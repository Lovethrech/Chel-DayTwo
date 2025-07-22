<script setup>
import AuthMainContent from './AuthMainContent.vue';
</script>

<template>
    <div class="check-out-main-ctn-main-ctn">
        <div class="check-out-main-ctn-mini-ctn">
            <AuthMainContent></AuthMainContent>
        </div>
    </div>
</template>

<style scoped>
.check-out-main-ctn-main-ctn{
    padding: 20px 40px;
    background-color: red;
    width:100%;
    height:100%;
    display:flex;
    justify-content: center;
    place-items: center;
}
.check-out-main-ctn-mini-ctn{
    background-color: orange;
    width:100%;
    min-height:100%;
    
}

@media screen and (max-width:950px) {
    .check-out-main-ctn-mini-ctn{
        width:90%;
        min-height:80vh;
    }
}
</style>