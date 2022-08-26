<template>
    <div class="cont position-relative">
        <img class="position-relative" src="../assets/bg-card-front.png" alt="">
        <div class="full-circle rounded-circle"></div>
        <div class="empty-circle rounded-circle"></div>
        <div class="txt text-white">
            <span v-if="cardNumber" class="fs-2 d-block mb-2">{{cardNumber}}</span>
            <span v-else class="fs-2 d-block mb-2">0000 0000 0000 0000</span>
            <span v-if="name">{{name}}</span>
            <span v-else>Francesco Ciano</span>
            <span class="exp-date position-absolute bottom-0">
                <span v-if="expirationDateMonth">{{expirationDateMonth}}</span><span v-else>00</span>/<span v-if="expirationDateYear">{{expirationDateYear}}</span><span v-else>00</span>
            </span>
        </div>
    </div>
</template>

<script>
export default {
    name:'FrontCard',
    props:{
        name:String,
        cardNumber:String,
        expirationDateMonth:String,
        expirationDateYear:String,
        }
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
            right: -3.2vw;
        }
    }
    &>*{
        position: absolute;
    }
}
</style>