<template>
    <div class="cont position-relative">
        <img class="position-relative" src="../assets/bg-card-front.png" alt="">
        <div class="full-circle rounded-circle"></div>
        <div class="empty-circle rounded-circle"></div>
        <div class="txt text-white">
            <span class="fs-2 d-block mb-2">0000 0000 0000 0000</span>
            <span>Femia Francesco</span>
            <span class="exp-date position-absolute bottom-0">00/00</span>
        </div>
    </div>
</template>

<script>
export default {
    name:'FrontCard'
}
</script>

<style lang="scss" scoped>
.cont{
    .full-circle{
        top: 4vh;
        left: 2vw;
        width: 3vw;
        height: 3vw;
        background-color: white;
    }
    .empty-circle{
        top: 6vh;
        left: 6vw;
        width: 2.4vh;
        height: 2.4vh;
        border: .2vh solid white ;
        background-color: rgba(255, 255, 255, 0);
    }
    .txt{
        width: max-content;
        top: 20vh;
        left: 2vw;
        .exp-date{
            right: -4vw;
        }
    }
}
.cont>*{
    position: absolute;
}
</style>