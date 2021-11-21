<template>
  <div>
    <header v-if="$route.meta.title">
      <h1 @click="counter = 0" >
        {{ $route.meta.title }} / {{ counter }}
      </h1>
    </header>
    <main>
      <router-view />
    </main>
  </div>
</template>

<script setup>
import { ref } from 'vue'

let counter = ref(0)

setInterval(() => {
  counter.value++
}, 1000)
</script>

<style>
body {
  font-family: 'Inter Roman', 'Helvetica Neue', Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
