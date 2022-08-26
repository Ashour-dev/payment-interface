<template>
    <div class="cont d-flex flex-wrap">
        <div class="form-group mb-4" id="card-number-field">
                <label for="name">cardholder name</label>
                <input type="text" class="form-control" id="name" placeholder="e.g. Francesco Ciano">
        </div>
        <div class="form-group mb-4" id="card-number-field">
                <label for="cardNumber">Card Number</label>
                <input type="text" class="form-control" id="cardNumber" placeholder="e.g. 1234 5678 9123 0000">
        </div>
        <div class="form-group w-50" id="expiration-date-field">
            <label class="w-100" for="expiration-date">EXP. Date (MM/YY)</label>
            <input type="text" class="form-control d-inline-block me-1" id="expiration-date-month" placeholder="MM">
            <input type="text" class="form-control d-inline" id="expiration-date-year" placeholder="YY">
        </div>
        <div class="form-group w-50 mb-4" id="cvv-field">
            <label for="cvv">CVV</label>
            <input type="text" class="form-control" id="cvv" placeholder="e.g. 123">
        </div>
        <button type="button" class="btn btn-dark py-2">confirm</button>
    </div>
</template>

<script>
export default {
    name:'DataEntery'
}
</script>

<style lang="scss" scoped>
    .cont{
        position: absolute;
        top: 12vh;
        right: 15vw;
        padding: 15vh 0;
        font-size: 18px;
        &>*{
            width: 100%;
        }
        & *{
            box-shadow: none !important;
        }
        width: 28vw;
        text-transform: uppercase;
        #expiration-date-month,#expiration-date-year{
            width: 47%;
        }
        label{
            margin-bottom: 7px;
        }
    }
</style>