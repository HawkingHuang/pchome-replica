<script setup>
import { onMounted } from 'vue'
import Header from './components/Header.vue'
onMounted(() => {
  feather.replace()
})
</script>

<template>
  <div>
    <Header />
  </div>
</template>

<style scoped>

</style>
