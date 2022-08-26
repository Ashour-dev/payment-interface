<template>
    <div class="cont position-relative mt-4">
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
    .cont{
        margin-left: 5vw;
        span{
            top: 15vh;
            right: 45.5vw;
        }
    }
</style>