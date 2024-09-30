<script setup>
    import {onMounted, ref} from "vue";
    import List from "./List.vue";
    let products = ref(null)

    onMounted(async() => {
        let response = await fetch("https://cwpeng.github.io/live-records-samples/data/products.json");
        let list = await response.json();
        products.value = list;
    })

</script>

<template>
    <main>
        <div>Products List</div>
        <div v-if="products === null">Loding...</div>
        <List v-else :products="products"></List>
    </main>
</template>

<style scoped>
</style>