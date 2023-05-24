<script setup lang="ts">
import {ref} from "vue";
import {invoke} from "@tauri-apps/api/tauri";
import {ElMessage} from "element-plus";

const greetMsg = ref("");
const name = ref("");

async function greet() {
  if (name.value.trim()) {
    // Learn more about Tauri commands at https://tauri.app/v1/guides/features/command
    greetMsg.value = await invoke("greet", {name: name.value});
  } else {
    ElMessage({
      type: 'error',
      message: 'Plz input a Name'
    })
  }
}
</script>
<!--Rename the file to be multiple name-->
<!--Or export it as multiple name like following code:-->
<!--<script lang="ts">-->
<!--export default {-->
<!--  name: "GreetItem"-->
<!--}-->
<!--</script>-->

<template>
  <el-form @submit.enter.prevent>
    <el-form-item>
      <el-input id="greet-input" v-model="name" placeholder="Enter a name..." />
    </el-form-item>
    <el-button type="primary" @click="greet()">Greet</el-button>
  </el-form>

  <p>{{ greetMsg }}</p>
</template>
