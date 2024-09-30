<script setup>
    import Main from "./Main.vue";
    import { ref } from "vue";
    let visible = ref(true);
    let hide  = function() {
        visible.value = false;
    };
    let show  = function() {
        visible.value = true;
    };
</script>

<template>
    <Main v-if="visible"></Main>
    <button @click="hide">hide</button>
    <button @click="show">show</button>
</template>

<style scoped>
</style>