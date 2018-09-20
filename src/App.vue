<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: "Karla", sans-serif;
  height: 100vh;
  width: 100vw;
}

body {
  background: url("./assets/background.jpg");
  background-attachment: fixed;
  background-size: cover;
  background-position: center center;
  background-repeat: no-repeat;
  width: 100vw;
  height: 100vh;
  margin: 0;
  padding: 0;
}
</style>
