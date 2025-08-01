<template>
  <h1>{{ message }}</h1>
  <Calc></Calc>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
import Calc from './components/Calc.vue';

const message = ref<string>("소고기")
</script>