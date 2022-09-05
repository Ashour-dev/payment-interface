<template>
    <div class="cont">
        <img class="position-relative w-100" src="../assets/bg-card-front.png" alt="">
        <div class="full-circle rounded-circle"></div>
        <div class="empty-circle rounded-circle"></div>
        <div class="txt text-white">
            <span v-if="cardNumber" class="my-fs-2 d-block mb-2">{{cardNumber}}</span>
            <span v-else class="my-fs-2 d-block mb-2">0000 0000 0000 0000</span>
            <span v-if="name" class=" text-uppercase">{{name}}</span>
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
@import '~bootstrap/scss/bootstrap';

// @media (min-width: 0){
//     .cont{
//         position: absolute;
//         top:20vh;
//         left: 5vw;
//         z-index: 2;
//         img{
//             // width: 90vw !important;
//             max-width: fit-content;
//         }
//     }
// }
.cont{
    .full-circle{
        top: 10%;
        left: 6%;
        width: 10%;
        padding-bottom: 10%;
        background-color: white;
    }
    .empty-circle{
        top: 16%;
        left:20%;
        width: 3.3%;
        padding-bottom: 3%;
        border: 1px solid white ;
        background-color: rgba(255, 255, 255, 0);
    }
    .txt{
        width: max-content;
        top: 57%;
        left: 6%;
        .exp-date{
            right: -13%;
        }
    }
    &>*{
        position: absolute;
    }
    position: relative;
}
@include media-breakpoint-up(md) {
    .cont{  
    width: 70%;
        .my-fs-2{
            font-size: 1.5rem;
        }
        .txt{
        top: 54%;
        }
    }
}
@include media-breakpoint-up(xl) {
    .cont{
        width: fit-content;
        .my-fs-2{
            font-size: 2rem;
        }
    }
}

</style>