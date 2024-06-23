<script setup>
    import {ref} from "vue";
    let stat = ref({
        title: "網站標題",
        className: "title"
    })
    const handler = function() {
        stat.value.title = "新的網站標題";
        stat.value.className = "title active";
    }
</script>

<template>
    <nav>基本的導覽列</nav>
    <main>
        <h1 :class="stat.className">{{ stat.title }}</h1>
        <button @click="handler">按鈕</button>
    </main>
</template>

<style scoped>
    .active { color: red; }
    main { background: #999; }
</style>