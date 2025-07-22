<script setup>
import { defineProps } from 'vue';

const {cardHolderName, nameType, nameFor, namePlaceholder, namePositionPlacement, name}=defineProps(['cardHoldeName', 'nameType', 'nameFor', 'namePlaceholder', 'namePositionPlacement', 'name']);
</script>

<template>
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
</template>