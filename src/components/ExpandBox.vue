<script setup>
import { ref } from 'vue'
const props = defineProps([`title`])
const showContent = ref(false)
</script>

<template>
  <div>
    <button @click="showContent = !showContent">mostrar</button>
    <div v-if="showContent" class="expand-box">
    <h1>{{ props.title }}</h1>
  </div>
  </div>
</template>

<style scoped>
.expand-box {
  height: 100%;
  padding: 20px;
  border: 1px solid black;
  box-shadow: 2px 2px 3px 3px gray;
  border-radius: 10px;
}
</style>
