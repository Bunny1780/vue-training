<script setup>
    import {ref} from "vue";
    let content = ref("");
    const clearContent = function() {
        content.value = ""
    }
    const interests = ref([])

    let color = ref("")
    let city = ref("")
</script>

<template>
    <nav>基本的導覽列</nav>
    <main>
        <h3>單行輸入框</h3>
        <input type="text" v-model="content" />
        <div>使用者輸入的文字：{{ content }}</div>
        <button @click="clearContent">清除</button>

        <h3>多選框</h3>
        角色扮演<input type="checkbox" value="rpg" v-model="interests">
        即時策略<input type="checkbox" value="rts" v-model="interests">
        動作遊戲<input type="checkbox" value="action" v-model="interests">
        <ul>你的興趣：
            <li v-for="interest in interests">{{ interest }}</li>
        </ul>

        <h3>單選框</h3>
        紅色<input type="radio" value="red" v-model="color" />
        綠色<input type="radio" value="green" v-model="color" />
        <div :class="color">你選的顏色</div>

        <h3>下拉式選單</h3>
        <div>你住在...{{ city }}</div>
        <select v-model="city">
            <option value="">請選擇</option>
            <option value="taipei">台北市</option>
            <option value="new taipei">新北市</option>
        </select>
    </main>
</template>

<style scoped>
    .red { color: red; }
    .green { color: green; }
    main { background: #c9c9c9; }
</style>