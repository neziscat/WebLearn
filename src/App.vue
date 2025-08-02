<template>
  <h1>{{ message }}</h1>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

const message = ref<string>("소고기")
</script>