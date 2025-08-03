<template>
  <div>
    <h1>{{ no }}</h1>
    <h1>o</h1>
  </div>
</template>

<script setup lang="ts">
import axios from 'axios';
import { onMounted, ref } from 'vue';

interface Data {
  data: tData;
}
interface tData {
  data: string;
}

const no = ref<string>();
onMounted(() => {
  axios.get("http://localhost:5000").then((res: Data) => {
    no.value = res.data.data;
    console.log("아ㅏㅏ")
  }).catch((error) => {
    console.log(error)
    no.value = `${error}`
  }).finally(() => {
    console.log("????")
  })
})
</script>