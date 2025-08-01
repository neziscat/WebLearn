<template>
  <div>
    <h1>{{ message }}</h1>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      message: "소고기"
    }
  },
  mounted() {
    console.log(this.message)
  }
}
</script>

<style scoped>
</style>
