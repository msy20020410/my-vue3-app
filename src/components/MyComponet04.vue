<template>
    <div class="my-component04">
        <!-- 点击按钮切换性别 -->
        <button @click="toggleSex">切换性别</button>
        <p>当前性别：{{ sex }}</p>
    </div>
</template>

<script setup>
import { reactive, ref } from 'vue'

const sex = ref('男')

function toggleSex() {
    sex.value = sex.value === '男' ? '女' : '男'
}


</script>

<style scoped></style>
