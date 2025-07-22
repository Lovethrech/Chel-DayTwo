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
    color:#b1a9a9;
}
.auth-main-content-mini-ctn-title{
    font-size: ;
    font-weight: 700;
}
.auth-main-content-mini-ctn-desc{
    font-size:14px;
}

@media screen and (max-width: 900px) {
    .auth-main-content-mini-ctn-title{
        font-size: ;
    }
    .auth-main-content-mini-ctn-desc{
        font-size: 12px;
    }
}
</style>