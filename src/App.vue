<script setup>
    const handler = function() {
        console.log("click")
    }
    const mouseover = function() {
        console.log("mouseover")
    }
</script>

<template>
    <nav>基本的導覽列</nav>
    <main>
        <button v-on:click="handler">按鈕</button>
        <button @click.once="handler" @mouseover="mouseover">按鈕</button>
        <a @click.prevent="handler" href="https://diswork.cc">Diswork</a>
    </main>
</template>

<style scoped>
    main { background: #999; }
</style>