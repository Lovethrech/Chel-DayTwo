<script setup>
import {ref} from "vue";

const namePositionPlacement=ref("50%");

</script>

<template>
    <form action="" class="auth-main-content-form-main-ctn">
        <div class="auth-main-content-form-input-and-label-ctn">
            <input type="text" id="" class="auth-main-content-form-input"/>
            <label for="" :style="{ top: namePositionPlacement }" class="auth-main-content-form-label"> Credit Card No:</label>
        </div>
    </form>
</template>

<style scoped>
.auth-main-content-form-main-ctn{
    margin-top: 3vh;
}
.auth-main-content-form-input-and-label-ctn{
    display:flex;
    flex-direction:column;
    position:relative;
    padding:1vh 3px;
    display:flex;
    margin: 4vh auto;
    font-size: 2vh;
    border-radius: 30px 0 10px 0;
}
.auth-main-content-form-label{
    position:absolute;
    font-size:16px;
    text-transform:capitalize;
    color:rgb(255, 255, 255);
    font-weight:200;
    transform: translateY(-50%);
    transition: all .5s;
}
.auth-main-content-form-input{
    outline:none;
    background: transparent;
    color:rgb(255, 255, 255);
    margin-right:0;
    width:100%;
    height:100%;
    outline:0;
    border:0;
    border-bottom:1px solid #ffffff;
    font-size:18px;
    padding: 2px 10px;
}
</style>