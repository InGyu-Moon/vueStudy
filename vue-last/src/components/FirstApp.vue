<template>
    <div>
        <h1 class="alert alert-info">FirstApp입니다.</h1>


        <h2>반응형 메시지</h2>
        <h3>{{ reactiveMessage }}</h3>
        <button v-on:click="btnReactiveMessage">Add Message</button>



        <h2>일반 메시지</h2>
        <h3>{{ normalMessage }}</h3>
        <button @click="btnNormalMessage">Add Message</button>
        
    </div>
</template>

<script>
import { isRef, onMounted, ref } from 'vue';

export default {
    setup () {

        const reactiveMessage=ref("Hello Reactive");
        const btnReactiveMessage=()=>{
            reactiveMessage.value=reactiveMessage.value+"!";
        }

        //반응형인지 검사
        console.log(isRef(reactiveMessage));


        let normalMessage = 'Normal Message';
        const btnNormalMessage=()=>{
            normalMessage=normalMessage+"!";
        }

        onMounted(()=>{
            console.log("onMounted");
        })

        return {
            reactiveMessage,
            normalMessage,
            btnReactiveMessage,
            btnNormalMessage
        }
    },
    methods:{

    }
}
</script>

<style lang="css" scoped>

</style>