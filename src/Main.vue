<script setup>
let emit = defineEmits(['update'])
let updateParentSubtitle = function() {
    emit("update")
}
</script>

<template>
    <main>
        <button @click="updateParentSubtitle">按鈕</button>
    </main>
</template>

<style scoped>
</style>