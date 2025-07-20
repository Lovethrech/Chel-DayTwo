<script setup>
import {ref} from "vue";

const namePositionPlacement=ref("50%");
const creditCardNo=ref("");

const iClick=()=>{
    if ((creditCardNo.value==="")||(email!=="")|| (age!=="")||(phoneNumber!=="") || (country!=="")){
        namePositionPlacement.value="-16px";
    }
    else{
        namePositionPlacement.value="50%";
    }
}
</script>

<template>
    <form action="" class="auth-main-content-form-main-ctn">
        <div class="auth-main-content-form-input-and-label-ctn">
            <input 
                v-model="creditCardNo" 
                type="text" 
                @click="iClick" 
                id="creditCardNo" 
                class="auth-main-content-form-input" 
            />
            <label 
                for="creditCardNo" 
                :style="{ top: namePositionPlacement }" 
                class="auth-main-content-form-label"
            >
                Credit Card No:
            </label>
        </div>
    </form>
</template>

<style scoped>
.auth-main-content-form-main-ctn{
    margin-top: 2vh;
    padding:2vh 2vw;
    border:2px solid #ffffff71;
    border-radius: 40px;
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