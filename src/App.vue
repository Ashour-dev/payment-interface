<template>
  <div id="app">
    <img class="desktopBackground position-absolute top-0" src="./assets/bg-main-desktop.png" alt="Background" />
    <div class="cards position-relative">
      <FrontCard :name="name" :cardNumber="cardNumber" :expirationDateMonth="expirationDateMonth" :expirationDateYear="expirationDateYear"/>
      <BackCard :cvv="cvv"/>
    </div>
    <DataEntery @name="assignName" @cardNumber="assignCardNum" @expirationDateMonth="assignExpirationMonth" @expirationDateYear="assignExpirationYear" @cvv="assignCvv"/>
  </div>
</template>

<script>
import FrontCard from "./components/FrontCard.vue";
import BackCard from "./components/BackCard.vue";
import DataEntery from "./components/DataEntery.vue";

export default {
  name: "App",
  components: {
    FrontCard,
    BackCard,
    DataEntery
  },
  data(){
    return{
      name:null,
      cardNumber:null,
      expirationDateMonth:null,
      expirationDateYear:null,
      cvv:null,
    }
  },
  methods:{
    assignName(name){
      this.name=name;
    },
    assignCardNum(cardNumber){
      this.cardNumber=cardNumber;
      console.log(cardNumber);
    },
    assignExpirationMonth(expirationDateMonth){
      this.expirationDateMonth=expirationDateMonth;
      console.log(expirationDateMonth)
    },
    assignExpirationYear(expirationDateYear){
      this.expirationDateYear=expirationDateYear;
      console.log(expirationDateYear)
    },
    assignCvv(cvv){
      this.cvv=cvv;
    }
  }

};
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap';
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500&display=swap');
#app {
  font-family: 'Space Grotesk', sans-serif;
  color: hsl(278, 68%, 11%);
  position: relative;
}
@media (min-width: 0) {
  .desktopBackground{
  height: 35vh;
  width: 100vw;
  }
}
@include media-breakpoint-up(md) {
  .desktopBackground{
  height: 100vh;
  width: 30vw;
}
.cards{
  padding-top: 14vh;
  padding-left: 12vw;
  width: fit-content;
  }
}
</style>
