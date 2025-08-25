<template>
    <div>
        <MyComponent16 v-model="fCount" />
        <hr>
        <!-- 父组件展示子组件的值 -->
        <p>父组件当前值: {{ fCount }}</p>

    </div>
</template>

<script setup>
// 引入子组件
import MyComponent16 from './MyComponent16.vue'
import { ref } from 'vue'
// 定义父组件的模型值
const fCount = ref(0)

</script>

<style scoped></style>