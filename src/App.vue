<script setup>
    const level = 3
    const arrays = ["HTML", "CSS", "JavaScript", "Vue.js"]
    const obj = {html: "HTML", css: "CSS", javascript: "JavaScript", vue: "Vue.js"}
</script>

<template>
    <nav>基本的導覽列</nav>
    <main>
        <div v-if="level === 3">大神</div>
        <div v-else-if="level === 2">資深</div>
        <div v-else-if="level === 1">菜鳥</div>
        <div v-else>零基礎</div>
        <ul>
            <li v-for="arr in arrays">{{ arr }}</li>
        </ul>
        <ul>
            <li v-for="(arr, index) in arrays">{{ index }} - {{ arr }}</li>
        </ul>
        <ul>
            <li v-for="(value, key) in obj">{{ key }} : {{ value }}</li>
        </ul>
    </main>
</template>

<style scoped>
    main { background: #999; }
</style>