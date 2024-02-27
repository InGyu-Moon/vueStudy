<template>
    <div>
        <h1 class="alert alert-info">ThirdApp입니다.</h1>

        <div v-if="isvisable" class="pink"></div>
        <div v-if="isvisable=false" class="green"></div>
        <div v-else class="orange"></div>



        <div v-if="count>1" class="pink">pink</div>
        <div v-else class="green">green</div>

        <button @click="count++">증가</button>
        <button @click="count--">감소</button>

    </div>
</template>

<script>
import { ref } from 'vue';

export default {
    setup () {

        const isvisable=false;
        const count=ref(0);
        

        return {
            isvisable,
            count
        }
    }
}
</script>

<style lang="css" scoped>
    .pink{
        background-color: pink;
    }
    .green{
        background-color: green;
        
    }
    .orange{
        background-color: orange;
        
    }
</style>