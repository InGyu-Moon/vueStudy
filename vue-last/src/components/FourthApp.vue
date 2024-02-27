<template>
    <div>
        <h1 class="alert alert-info">FourthApp입니다.</h1>

        <li v-for="fruit in fruitArray" :key="fruit">{{ fruit }}</li>




    </div>
</template>

<script>
export default {
    setup () {
        const fruitArray=['apple','banana','orange'];
        const infoArray=[
            {id:0,user:'영수'},
            {id:1,user:'일수'},
            {id:2,user:'이수'},
            {id:3,user:'삼수'}
        ]

        return {
            fruitArray,
            infoArray
        }
    }
}
</script>

<style lang="css" scoped>

</style>