<script setup>
import Textfield from "./Textfield.vue";
</script>
<template>
  <div class="w-full border justify-center p-3 flex items-center">
    <v-avatar size="40px" color="white">
      <img src="/ai.png" alt="alt" />
    </v-avatar>
  </div>

  <div class="text-h4 text-center font-extrabold">
    AI power search optimization
  </div>
  <div class="text-caption text-center font-extrabold mt-1 p-1">
    search for answers,news,trends,fassion and much more with our powerful ai
    tool
  </div>
  <div class="wfull p-1">
    <Textfield className="bg-slate-300" />
    <v-btn outline class="w-full mt-1" color="info">search</v-btn>
  </div>
  <div class="w-full flex flex-col items-center mt-2">
    <div class="rounded-full w-16 h-16 border-2 border-white">
      <v-avatar size="100%" color="white">
        <img src="/b.jpg" alt="alt" />
      </v-avatar>
    </div>
    <div class="text-caption p-1"></div>
    <button
      class="bg-yellow-500 transition-all ease-in hover:shadow-2xl shadow-green-400 p-2 rounded-xl mt-1 w-3/5 text-white">
      news later
    </button>
  </div>
</template>
