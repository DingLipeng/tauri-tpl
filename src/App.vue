<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import Greet from "./components/GreetItem.vue";
</script>

<template>
  <div class="container">
    <h1>A Tauri Template!</h1>
    <p>Step 0: Input a name to communicate with Rust backend</p>
    <Greet />
  </div>
</template>

<style scoped></style>
