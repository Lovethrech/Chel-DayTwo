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
    padding: 0 40px;
    width:100%;
    height:100%;
    display:flex;
    justify-content: center;
    place-items: center;
}
.check-out-main-ctn-mini-ctn{
    width:100%;
    height:100%;
}

@media screen and (max-width:980px) {
    .check-out-main-ctn-main-ctn{
        padding: 20px 10px;
    }
    .check-out-main-ctn-mini-ctn{
        width:90%;
    }
}
</style>