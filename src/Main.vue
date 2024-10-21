<script setup>
    import {onMounted, ref} from "vue";
    import List from "./List.vue";
    // let products = ref(null)

    // onMounted(async() => {
    //     let response = await fetch("https://cwpeng.github.io/live-records-samples/data/products.json");
    //     let list = await response.json();
    //     products.value = list;
    // })
    const products = [
        {name:"Pixel", price:17700, description:"最新的 Pixel 手機。"},
        {name:"Chromecast", price:1500, description:"在大螢幕上播放喜歡的影片。"},
        {name:"Pixel Book", price:12000, description:"最新的 Chromebook 產品。"},
    ]

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