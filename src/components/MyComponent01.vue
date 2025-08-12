<template>
    <div class="my-component01">
        计数器:{{ count }}
        <button @click="increment">+</button>
        <button @click="decrement">-</button>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)

// 创建count递增函数
const increment = () => {
    count.value++
}

// 创建count递减函数
const decrement = () => {
    count.value--
}

</script>

<style scoped></style>
