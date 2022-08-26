<template>
  <div id="app">
    <img class="desktopBackground" src="./assets/bg-main-desktop.png" alt="Background" />
    <div class="cards d-flex flex-column ">
      <FrontCard/>
    </div>
  </div>
</template>

<script>
import FrontCard from "./components/FrontCard.vue";

export default {
  name: "App",
  components: {
    FrontCard
  },
};
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;

}
.desktopBackground{
  height: 100vh;
  width: 30vw;
}
.cards{
  position: absolute;
  top: 30vh;
  left: 10vw;

}
</style>
