<script setup>
import { defineProps } from 'vue';

const {cardHolderName, nameType, nameFor, namePlaceholder, namePositionPlacement, name, iClick}=defineProps(['cardHoldeName', 'nameType', 'nameFor', 'namePlaceholder', 'namePositionPlacement', 'name', 'iClick']);
const iClickCardHolderName=()=>{
    if ((cardHolderName.value==="")){
        namePositionPlacement.value="-16px";
    }
    else{
        namePositionPlacement.value="50%";
    }
}
</script>

<template>
    <div class="auth-main-content-form-input-and-label-ctn">
        <input 
            v-model="cardHolderName" 
            :type="creditCardDetails[0].nameType" 
            @click="iClickCardHolderName" 
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
</template>