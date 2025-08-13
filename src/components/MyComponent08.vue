<template>
    <div class="my-component08">
        <!-- 创建用户输入 -->
        <input type="text" v-model="input" placeholder="请输入内容" />
        <hr>
        <!-- 创建用户信息输入 -->
        <input type="text" v-model="personInfo.name" placeholder="请输入姓名" /><br>
        <input type="number" v-model="personInfo.age" placeholder="请输入年龄" />
    </div>
</template>

<script setup>
// 引入侦听器函数
import { reactive, ref, watch, watchEffect } from 'vue'

const input = ref('')
const personInfo = reactive({
    name: '张三',
    age: 18
})

// 监听用户输入
watch(input,
    (newValue, oldValue) => {
        console.log(`用户将输入框的值从 ${oldValue} 改为 ${newValue}`)
    },
    { immediate: true })

// 使用watchEffect函数监听
watchEffect(() => {
    console.log(`姓名修改为了: ${personInfo.name}`)
    console.log(`年龄修改为了: ${personInfo.age}`)
})
</script>

<style scoped></style>