<template>
    <div class="cont mt-4">
        <span v-if="cvv" class="position-absolute text-white">{{cvv}}</span>
        <span v-else class="position-absolute text-white">000</span>
        <img class="w-100" src="../assets/bg-card-back.png" alt="">
    </div>
</template>

<script>
export default {
    name:'BackCard',
    props:{cvv:String}
}
</script>

<style lang="scss" scoped>
@import '~bootstrap/scss/bootstrap';
.cont{
        margin-left: 5vw;
        position: relative;
        span{
            top: 44%;
            right: 12%;
        }
    }
@include media-breakpoint-down(md){
.cont{
    position: absolute;
    top:0;
    right: 2vw;
    z-index: 1;
    width: 70%;
    margin-left:auto;
    font-size: 3vw;
}
}
@include media-breakpoint-up(md) {
    .cont{  
    width: 70%;
    font-size: small;
    }
}
@include media-breakpoint-up(xl) {
    .cont{
        width: fit-content;
        font-size: large;
    }
}
</style>