<script setup lang="ts">
import Hello from "./components/Hello.vue";
import Header from "./components/header.vue";

const name: string = "mutangizi r";
</script>

<template>
  <div
    class="w-full min-h-96 h-screen flex flex-col relat items-center bg-[url('/hello1.jpg')] bg-cover bg-center">
    <Header />
    <Hello />
  </div>
</template>

<style scoped></style>
