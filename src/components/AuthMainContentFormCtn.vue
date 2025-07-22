<script setup>
import {ref} from "vue";
import creditCardDetails from '@/data/creditCardDetails.json';

const namePositionPlacement=ref("50%");
const expirationDateNamePositionPlacement=ref("-16px");
const cardHolderName=ref("");
const creditCardNo=ref("");
const securityCode=ref("");
const billingAddress=ref("");
const emailAddress=ref("");
const saveCard=ref();
const agreeToTAndC=ref(true);

const iClick=()=>{
    if ((cardHolderName.value==="")||(creditCardNo.value==="")|| (age!=="")||(phoneNumber!=="") || (country!=="")){
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
                v-model="cardHolderName" 
                :type="creditCardDetails[0].nameType" 
                @click="iClick" 
                :id="creditCardDetails[0].nameFor" 
                :placeholder="creditCardDetails[0].namePlaceholder"
                class="auth-main-content-form-input" 
            />
            <label 
                :for="creditCardDetails[0].nameFor" 
                :style="{ top: namePositionPlacement }" 
                class="auth-main-content-form-label"
            >
                {{ creditCardDetails[0].name }}
            </label>
        </div>
        <div class="auth-main-content-form-input-and-label-ctn">
            <input 
                v-model="creditCardNo" 
                :type="creditCardDetails[1].nameType" 
                @click="iClick" 
                :id="creditCardDetails[1].nameFor" 
                :placeholder="creditCardDetails[1].namePlaceholder"
                class="auth-main-content-form-input" 
            />
            <label 
                :for="creditCardDetails[1].nameFor" 
                :style="{ top: namePositionPlacement }" 
                class="auth-main-content-form-label"
            >
                {{ creditCardDetails[1].name }}
            </label>
        </div>
        <div class="auth-main-content-form-input-and-label-ctn">
            <input 
                v-model="cardHolderName" 
                :type="creditCardDetails[2].nameType" 
                @click="iClick" 
                :id="creditCardDetails[2].nameFor" 
                :placeholder="creditCardDetails[2].namePlaceholder"
                class="auth-main-content-form-input" 
            />
            <label 
                :for="creditCardDetails[2].nameFor" 
                :style="{ top: expirationDateNamePositionPlacement }" 
                class="auth-main-content-form-label"
            >
                {{ creditCardDetails[2].name }}
            </label>
        </div>
        <div class="auth-main-content-form-input-and-label-ctn">
            <input 
                v-model="securityCode" 
                :type="creditCardDetails[3].nameType" 
                min="3"
                max="3"
                @click="iClick" 
                :id="creditCardDetails[3].nameFor" 
                :placeholder="creditCardDetails[3].namePlaceholder"
                class="auth-main-content-form-input" 
            />
            <label 
                :for="creditCardDetails[3].nameFor" 
                :style="{ top: namePositionPlacement }" 
                class="auth-main-content-form-label"
            >
                {{ creditCardDetails[3].name }}
            </label>
        </div>
        <div class="auth-main-content-form-input-and-label-ctn">
            <input 
                v-model="billingAddress" 
                :type="creditCardDetails[4].nameType" 
                min="3"
                max="3"
                @click="iClick" 
                :id="creditCardDetails[4].nameFor" 
                :placeholder="creditCardDetails[4].namePlaceholder"
                class="auth-main-content-form-input" 
            />
            <label 
                :for="creditCardDetails[4].nameFor" 
                :style="{ top: namePositionPlacement }" 
                class="auth-main-content-form-label"
            >
                {{ creditCardDetails[4].name }}
            </label>
        </div>
        <div class="auth-main-content-form-input-and-label-ctn">
            <input 
                v-model="emailAddress" 
                :type="creditCardDetails[5].nameType" 
                @click="iClick" 
                :id="creditCardDetails[5].nameFor" 
                :placeholder="creditCardDetails[5].namePlaceholder"
                class="auth-main-content-form-input" 
            />
            <label 
                :for="creditCardDetails[5].nameFor" 
                :style="{ top: namePositionPlacement }" 
                class="auth-main-content-form-label"
            >
                {{ creditCardDetails[5].name }}
            </label>
        </div>
        <div class="auth-main-content-form-input-and-label-ctn-check-box">
            <input 
                v-model="saveCard" 
                :type="creditCardDetails[6].nameType" 
                @click="iClick" 
                :id="creditCardDetails[6].nameFor" 
                class="auth-main-content-form-input-check-box" 
            />
            <label 
                :for="creditCardDetails[6].nameFor" 
                :style="{ top: namePositionPlacement }" 
                class="auth-main-content-form-label-check-box"
            >
                {{ creditCardDetails[6].name }}
            </label>
        </div>
        <div class="auth-main-content-form-input-and-label-ctn-check-box">
            <input 
                v-model="agreeToTAndC" 
                :type="creditCardDetails[7].nameType" 
                @click="iClick" 
                :id="creditCardDetails[7].nameFor" 
                class="auth-main-content-form-input-check-box" 
            />
            <label 
                :for="creditCardDetails[7].nameFor" 
                :style="{ top: namePositionPlacement }" 
                class="auth-main-content-form-label-check-box"
            >
                {{ creditCardDetails[7].name }}
            </label>
        </div>
        <button type="submit" class="auth-main-content-form-input-and-label-ctn-submit-btn">
            Make payment
        </button>
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
.auth-main-content-form-input::placeholder{
    text-align: right;
    color:rgb(255, 255, 255);
    font-size: 12px;
}
.auth-main-content-form-input-and-label-ctn-check-box{
    
}
.auth-main-content-form-input-and-label-ctn-submit-btn{
    width:100%;
    background-color:#fff;
}


@media screen and (max-width:1290px) {
    .auth-main-content-form-input::placeholder:nth-child(4){
        display:none;
    }
}
</style>