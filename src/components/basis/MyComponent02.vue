<template>
    <div class="my-component02">
        <!-- 展示姓名与年龄 -->
        <p>姓名: {{ person.name }}</p>
        <p>年龄: {{ person.age }}</p>
        <hr>
        <button @click="person.name = '李四'">变李四</button>
        <button @click="person.age++">年龄+1</button>
        <button @click="reset">重置</button>
    </div>
</template>

<script setup>
// 引入ractive函数
import { reactive } from 'vue'

// 创建一个响应式对象
const person = reactive({
    name: '张三',
    age: 30
})

// 重置函数
const reset = () => {
    person.name = '无名氏'
    person.age = 99
}
</script>

<style scoped></style>
