<script setup>
    import Nav from "./Nav.vue";
    import Main from "./Main.vue";
    import { ref } from "vue";

    // 標準事件處理
    let text = ref("測試文字");
    let change = function() {
        text.value = "修改文字"
    }
</script>

<template>
    <Nav></Nav>
    <!-- <Main></Main> -->
    <Main @Myevent="change"></Main> <!-- 自訂事件處理 -->
    <div>{{ text }}</div>

    <!-- 標準事件處理 -->
    <!-- <button @click="change">按鈕</button> -->
</template>

<style scoped>
</style>