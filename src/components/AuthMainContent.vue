<script setup>
import AuthMainContentFormCtn from './AuthMainContentFormCtn.vue';
</script>

<template>
    <div class="auth-main-content-main-ctn">
        <div class="auth-main-content-mini-ctn">
            <h1 class="auth-main-content-mini-ctn-title">
                Payment Method
            </h1>
            <p class="auth-main-content-mini-ctn-desc">
                Fill out all input field for successful checkout payment
            </p>
            <AuthMainContentFormCtn></AuthMainContentFormCtn>
        </div>
    </div>
</template>

<style scoped>
.auth-main-content-main-ctn{
    color:#fff;

}
</style>