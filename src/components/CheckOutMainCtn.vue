<script setup>
import AuthMainBgCtn from './AuthMainBgCtn.vue';
</script>

<template>
    <div class="check-out-main-ctn-main-ctn">
        <div class="check-out-main-ctn-mini-ctn">
            <AuthMainBgCtn></AuthMainBgCtn>
        </div>
    </div>
</template>

<style scoped>
.check-out-main-ctn-main-ctn{
    width:100%;
    height:100%;
    display:flex;
    justify-content: center;
    place-items: center;
}
.check-out-main-ctn-mini-ctn{
    background-color: azure;
    width:50%;
    height:40vh;
    display:flex;
    justify-content: center;
}
</style>