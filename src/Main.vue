<script setup>
    import {onMounted, onUpdated, onUnmounted, ref} from "vue";

    onMounted(function() {
        console.log("onMounted")
    })
    onUpdated(function() {
        console.log("onUpdate")
    })
    onUnmounted(function() {
        console.log("onUnmounted")
    })
    let text = ref("Main Text");
    let update = function() {
        text.value = "Change Text";
    }
</script>

<template>
    <main>
        <div>{{ text }}</div>
        <button @click="update">change text</button>
    </main>
</template>

<style scoped>
</style>