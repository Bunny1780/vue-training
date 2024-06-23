<script setup>
    import {ref} from "vue";
    let title = ref("網站標題")
    const handler = function() {
        console.log("click")
        title.value = "新的網站標題"
    }
</script>

<template>
    <nav>基本的導覽列</nav>
    <main>
        <h1>{{ title }}</h1>
        <button @click="handler">按鈕</button>
    </main>
</template>

<style scoped>
    main { background: #999; }
</style>