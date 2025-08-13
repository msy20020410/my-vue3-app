<template>
    <div class="my-component09">
        <input type="text" ref="my-input" placeholder="请输入内容" />
        <hr>
        <ul>
            <li v-for="item in list" :key="item" ref="items">{{ item }}</li>
        </ul>
    </div>
</template>

<script setup>
// 引入使用模板引用函数
import { useTemplateRef, onMounted, ref } from 'vue'

const list = ref([1, 2, 3, 4, 5])

const input = useTemplateRef("my-input")
const itemRefs = useTemplateRef("items")



// 此操作会在页面加载时, 自动聚焦到输入框
onMounted(() => {
    input.value.focus()
})

onMounted(() => {
    console.log(itemRefs.value)
})



</script>

<style scoped></style>