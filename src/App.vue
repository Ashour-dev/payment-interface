<template>
  <div id="app">
    <img class="desktopBackground position-absolute top-0" src="./assets/bg-main-desktop.png" alt="Background" />
    <div class="cards">
      <FrontCard/>
      <BackCard/>
    </div>
  </div>
</template>

<script>
import FrontCard from "./components/FrontCard.vue";
import BackCard from "./components/BackCard.vue";

export default {
  name: "App",
  components: {
    FrontCard,
    BackCard
  },
};
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  position: relative;
}
.desktopBackground{
  height: 100vh;
  width: 30vw;
}
.cards{
  padding: 14vh 15vw;
}
</style>
