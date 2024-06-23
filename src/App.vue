<script setup>
    const message = "Hello Vue";
    const messageHtml = "<u>Hello Vue</u>";
    const name = "content"
    const check = false
</script>

<template>
    <nav>基本的導覽列</nav>
    <div>{{ message }}</div> <!-- 插入變數 -->
    <div v-html="messageHtml"></div> <!-- 插入html -->
    <div>{{ message.toUpperCase() }}</div> <!-- 插入程式語句 -->
    <div v-bind:class="name">插入屬性</div> <!-- 插入屬性 -->
    <div :class="check?'dark':'light'">插入屬性使用三元運算</div>
</template>

<style scoped>
    main { background: #999; }
    .dark { color: #333; }
    .light { color: #c9c9c9; }
</style>