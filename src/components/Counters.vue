<script setup>
import { reactive, ref, watch } from 'vue';
const counterReactive = reactive({
    counter1: 0, counter2: 0,
});
const date = ref(new Date().toUTCString());

// function counterHandler(event){
//     console.log();
// }

    watch(() => {
        setInterval(()=>{date.value = new Date().toUTCString()}, 1000)
    });
const counterRef = ref(0);
</script>

<template>
    <button @click="counterReactive .counter1++">Plus</button>
    <h3>{{ counterReactive.counter1 }}</h3>
    <button @mousemove="counterReactive .counter2 = $event.clientX">MouseMove</button>
    <h3>{{ counterReactive.counter2 }}</h3>
    <button @click="counterRef++">Plus {{ counterRef }}</button>

    <h1>{{ date }}</h1>
</template>

<style lang="scss" scoped>

</style>