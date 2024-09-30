<script setup>
    import {onMounted, onUnmounted, ref} from "vue";

    onMounted(function() {
        console.log("onMounted")
    })
    let schedule;
    onUnmounted(function() {
        window.clearInterval(schedule)
        console.log("onUnmounted")
    })
    let text = ref("Main Text");
    let update = function() {
        text.value = "Change Text";
    }
    let count = ref(0)
    schedule = window.setInterval(function() {
        count.value += 1
        console.log("+1");
    }, 1000)
</script>

<template>
    <main>
        <div>{{ text }}</div>
        <button @click="update">change text</button>
    </main>
</template>

<style scoped>
</style>