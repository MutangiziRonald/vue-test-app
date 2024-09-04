<script setup lang="ts">
import { ref } from "vue";
import Textfield from "./Textfield.vue";
const value = ref("");

const links: {
  name: string;
  link: string;
}[] = [
  { name: "home", link: "/" },
  { name: "Blogs", link: "/blogs" },
  { name: "news", link: "/news" },
  { name: "insights", link: "/insites" },
];
const currentPath = window.location.pathname;
</script>
<template>
  <header class="w-full flex shadow-md items-center h-20 px-3">
    <div class="w-auto text-lg">
      <img src="/logo2.png" class="h-16" alt="" srcset="" />
    </div>
    <div class="flex-1 flex items-center justify-end p-1 px-2">
      <div class="flex items-center mr-3">
        <a
          :class="[
            ' relative capitalize  hover:text-blue-600 m-2 text-md',
            link.link != currentPath ? 'active text-blue-50' : ' text-white',
          ]"
          v-for="link in links"
          :href="link.link"
          :key="link.link"
          >{{ link.name }}</a
        >
      </div>
      <div class="flex">
        <Textfield :value="value"></Textfield>
        <v-avatar size="40px" color="red" class="ml-2">
          <img src="/logo.png" alt="alt" />
        </v-avatar>
      </div>
    </div>
  </header>
</template>
<style scoped>
.active::after {
  content: "";
  width: 100%;
  height: 4px;

  position: absolute;
  bottom: -5px;
  left: 0;
  transition: 1s ease-in-out;
}
.active:hover::after {
  width: 50%;
  background-color: rgb(104, 233, 226);
}
header {
  backdrop-filter: blur(10px);
}
</style>
