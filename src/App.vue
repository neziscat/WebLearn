<template>
  <div class="messagebox">
    <h1>잔디 심은 내역</h1>
    <input class="input" v-model="id"></input>
    <button class="button" @click="setId">확인</button>
  </div>
  <img :src="grass" @error="onImageError"/>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

const id = ref<string>("");
const grass = ref<string>("");

function setId() {
    grass.value = `https://ghchart.rshah.org/${encodeURIComponent(id.value)}`
  
}
function onImageError() {
  alert('이미지를 불러올 수 없습니다. ID가 잘못됐거나 존재하지 않습니다.')
  grass.value = ''
}
</script>