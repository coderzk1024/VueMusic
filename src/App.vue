<template>
  <div id="app">
    <Navbar />
    <div id="homeMain">
      <LeftBar />
      <router-view />
    </div>
    <div id="mainFooter"></div>
  </div>
</template>

<script>
import Navbar from "@/views/header/NavBar";

import LeftBar from "@/views/left/LeftBar";
export default {
  name: "App",
  components: { Navbar, LeftBar },
};
</script>

<style lang="scss">
@import "~@/assets/css/base.css";
#app {
  width: 1024px;
  height: 670px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  box-shadow: 0 0 10px #c8c8c8;

  display: flex;
  flex-direction: column;
}
#homeMain {
  flex: 1;
  display: flex;
}
#mainFooter {
  height: 74px;
}
</style>
