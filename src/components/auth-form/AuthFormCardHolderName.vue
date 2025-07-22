<script setup>
import { ref, defineProps } from 'vue';

const {cardHolderName, nameType, nameFor, namePlaceholder, name}=defineProps(['cardHoldeName', 'nameType', 'nameFor', 'namePlaceholder', 'name']);
const namePositionPlacement=ref("50%");

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
            :type="nameType" 
            @click="iClickCardHolderName" 
            :id="nameFor" 
            :placeholder="namePlaceholder"
            class="auth-main-content-form-input" 
        />
        <label 
            :for="nameFor" 
            :style="{ top: namePositionPlacement }" 
            class="auth-main-content-form-label"
        >
            {{ name }}
        </label>
    </div>
</template>