<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Intro from "./components/Intro.vue";
import Profile from "./components/Profile.vue";
import Projects from "./components/Projects.vue";
import Music from "./components/Music.vue";
</script>

<template>
  <Intro />
  <Profile />
  <Projects />
  <Music />
</template>

<style>
#app {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Oxygen",
    "Ubuntu", "Cantarell", "Fira Sans", "Droid Sans", "Helvetica Neue",
    sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}

button {
  flex: 1 1 auto;
  margin: 10px;
  padding: 10px;
  text-align: center;
  font-size: 1em;
  transition: 0.5s;
  background-size: 200% auto;
  color: white;
  /* text-shadow: 0px 0px 10px rgba(0,0,0,0.2);*/
  box-shadow: 0 0 20px #eee;
  border-radius: 10px;
  background-image: linear-gradient(
    to right,
    #fbc2eb 0%,
    #a6c1ee 51%,
    #fbc2eb 100%
  );
}

button:hover {
  cursor: pointer;
  background-position: right center; /* change the direction of the change here */
}
</style>
