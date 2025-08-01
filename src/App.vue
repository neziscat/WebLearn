<template>
  <div>
    <h1>{{ message }}</h1>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      message: "소고기 world!"
    }
  },

  // `mounted` is a lifecycle hook which we will explain later
  mounted() {
    console.log(this.data().message)
  }
}
</script>

<style scoped>
</style>
