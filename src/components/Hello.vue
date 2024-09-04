<script setup>
import Ai from "./Ai.vue";
</script>
<template>
  <div class="flex-1 flex hello overflow-hidden">
    <div
      class="flex-1 h-full flex flex-col items-center justify-center py-6 relative">
      <div class="absolute w-72 h-72 rounded-full ball"></div>
      <div class="absolute w-72 h-72 rounded-full ball1"></div>
      <h3
        class="text-3xl text-white mb-6 [text-shadow:_0_4px_8px_#00BCD4] md:text-2xl leading-snug font-manrope font-extrabold">
        👋 Hello! Welcome to LOBlog platform
      </h3>
      <p class="lg:w-7/12">
        Hey there! 👋 We’re thrilled to have you here at LOBlog, your go-to spot
        for inspiring stories, tech tips, delicious recipes, etc. 🚀
      </p>
      <p class="lg:w-7/12">
        Dive into our latest posts where we share [mention types of content,
        e.g., tips, tricks, and insights on various topics]. Whether you’re here
        to discover new ideas, learn something new, or just relax, we’ve got
        something just for you! 💡✨
      </p>
      <p class="lg:w-7/12">
        Don’t forget to subscribe and follow us on [mention social media
        channels if applicable] to stay updated on our newest content. We’re
        excited to embark on this journey with you! 🌟
      </p>
    </div>

    <div
      class="w-72 m-4 box mr-6 rounded-lg shadow-blue-600 shadow-2xl bg-white min-w-72">
      <Ai />
    </div>
  </div>
</template>
<style scoped>
.hello {
  width: 100%;
  border-image: fill 0 linear-gradient(#0001, #000);
}
.box {
  background: url("/bg.svg") no-repeat;
  background-position: bottom;
}
p {
  color: aliceblue;
  margin-top: 20px;

  text-align: center;
}
.ball {
  background-color: rgba(240, 248, 255, 0.342);
  animation: anim infinite 40s linear;
}
.ball1 {
  background-color: rgba(240, 248, 255, 0.123);
  animation: anim2 infinite 30s linear;
  animation-delay: 3s;
}
@keyframes anim2 {
  0% {
    opacity: 0;
    bottom: -212px;
    left: -100px;
  }
  100% {
    bottom: 100%;
    left: 150%;
    opacity: 1;
  }
}
@keyframes anim {
  0% {
    opacity: 0;
    top: -212px;
    right: -100px;
  }
  100% {
    top: 100%;
    right: 100%;
    opacity: 1;
  }
}
</style>
