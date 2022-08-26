<template>
    <div class="cont">
        <img id="card" src="../assets/bg-card-front.png" alt="">
        <div class="full-circle rounded-circle"></div>
    </div>
</template>

<script>
export default {
    name:'FrontCard'
}
</script>

<style lang="scss" scoped>
.cont{
    #card{
        position: absolute;
    }
    .full-circle{
        position: absolute;
        top: 2vw;
        left: 2vw;
        width: 3vw;
        height: 3vw;
        background-color: white;
    }
}
</style>