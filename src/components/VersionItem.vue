<script setup lang="ts">
import {ref} from "vue";
import {getTauriVersion} from "@tauri-apps/api/app";

const tauriVersion = ref("");
getTauriVersion().then(version => {
  tauriVersion.value = version
})
</script>

<template>
  <p>Tauri v{{ tauriVersion }}</p>
</template>
