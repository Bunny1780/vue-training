<script setup>
    import Nav from "./Nav.vue";
    import Main from "./Main.vue";
    import { ref } from "vue";
    // 自訂事件處理二
    let subtitle = ref("這是副標題");
    let updatesubtitle = function() {
        subtitle.value = "這是新的副標題"
    }
</script>

<template>
    <Nav
        title="這是主標題"
        :subtitle="subtitle"
    ></Nav>
    <Main @update="updatesubtitle"></Main> 
    <div>{{ text }}</div>
</template>

<style scoped>
</style>