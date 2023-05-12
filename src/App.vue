<template>
  <div id="app">
    <NavBar />
    <router-view />
  </div>
</template>

<script>
import NavBar from "@/components/NavBar"
export default {
  components: { NavBar }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans&display=swap');
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  :root {
    --color: #4eb5d6;
    --bg: #0f152e;
  }
  body {
    background-color: var(--bg);
    font-family: 'Open Sans', sans-serif;
    margin: 0;
  }
  a {
    text-decoration: none;
    color: white;
    transition: 0.8s;
  }
  a:hover {
    color: var(--color);
  }
  #app {
    width: 100%;
  }
</style>