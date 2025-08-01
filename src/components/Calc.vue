<template>
    <input type="number" v-model.number="aRef"></input>
    <input type="number" v-model.number="bRef"></input>
    <button @click="add">+</button>
    <button @click="subtract">-</button>
    <button @click="multiplication">×</button>
    <button @click="division">÷</button>
    <h1>{{ answer }}</h1>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const aRef = ref<number>(0)
const bRef = ref<number>(0)
const answer = ref<number>(0);

function add() {
    answer.value = aRef.value + bRef.value;
}
function subtract() {
    answer.value = aRef.value - bRef.value;
}
function multiplication() {
    answer.value = aRef.value * bRef.value;
}
function division() {
    answer.value = aRef.value / bRef.value;
}


</script>