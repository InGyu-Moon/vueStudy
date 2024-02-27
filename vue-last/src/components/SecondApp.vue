<template>
    <div>
        <h1 class="alert alert-info">SecondApp입니다.</h1>

        <h2>{{ num }}</h2>
        <button class="btn btn-info" @click="btnClick1">증가</button>

        <h2>{{ msg }}</h2>
        <button class="btn btn-info" @click="btnClick2">메시지 추가</button>
    </div>
</template>

<script>
import { ref } from 'vue';

export default {
    setup () {
        
        const num = ref(0);
        const btnClick1=()=>{
            num.value++;
        }

        const msg=ref('hello');
        const btnClick2=()=>{
            msg.value=msg.value+"!";
        }
        



        return {
            msg,
            num,
            btnClick1,
            btnClick2
        }
    },
    methods:{

    }
}
</script>

<style lang="css" scoped>

</style>