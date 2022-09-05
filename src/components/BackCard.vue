<template>
    <div class="cont mt-4">
        <span v-if="cvv" class="position-absolute text-white">{{cvv}}</span>
        <span v-else class="position-absolute text-white">000</span>
        <img src="../assets/bg-card-back.png" alt="">
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

@media (min-width: 0){
    .cont{
        position: absolute;
        top: 0;
        right: 0;
        width: 90vw;
        z-index: 1;
    }
}
@include media-breakpoint-up(md) {
    .cont{
        margin-left: 5vw;
        width: fit-content;
        position: relative;
        span{
            top: 44%;
            right: 12%;
        }
    }
    }
</style>