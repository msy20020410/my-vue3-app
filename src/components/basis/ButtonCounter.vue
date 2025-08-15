<template>
    <div>
        <button @click="increment">+</button>
        <p>当前计数：{{ count }}</p>
        <button @click="decrement">-</button>
    </div>
</template>

<script setup>
import { ref } from 'vue'
const count = ref(0)

function increment() {
    count.value++
}

function decrement() {
    count.value--
}

</script>

<style lang="scss" scoped></style>