<script setup>
import axios from "axios";
import HelloWorld from "./components/HelloWorld.vue";

const handleClick = () => {
  console.log("发了，还没回");
  axios
    .post("https://2kgvgeaq4e.us.aircode.run/hello", {
      hi: undefined,
    })
    .then((res) => {
      console.log("回复了", res);
    });
};
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="快速搭建一个线上网站的前端" />
  <button @click="handleClick">发个 hi</button>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
