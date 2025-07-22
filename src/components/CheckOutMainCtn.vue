<script setup>
// import AuthMainBgCtn from './AuthMainBgCtn.vue';
import AuthMainContentCtn from './AuthMainContentCtn.vue';
</script>

<template>
    <div class="check-out-main-ctn-main-ctn">
        <div class="check-out-main-ctn-mini-ctn">
            <!-- <AuthMainBgCtn></AuthMainBgCtn> -->
            <AuthMainContentCtn></AuthMainContentCtn>
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
    width:60%;
    min-height:100%;
    
}

@media screen and (max-width:950px) {
    .check-out-main-ctn-mini-ctn{
        width:90%;
        min-height:80vh;
    }
}
</style>