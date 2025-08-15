<template>
    <div class="my-component06">
        <!-- 内联事件处理器 -->
        <button @click="count++">{{ count }}</button>
        <hr>
        <!-- 方法事件处理器 -->
        <button @click="greet">Greet</button>

    </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)

const name = ref('Vue 3')

// 定义greet方法
const greet = () => {
    alert(`Hello! ${name.value}`);
}

</script>

<style scoped></style>