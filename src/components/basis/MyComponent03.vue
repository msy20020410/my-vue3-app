<template>
    <div class="my-component03">
        <!-- 在模板中引用计算属性 -->
        {{ publishedBooks }}
    </div>
</template>

<script setup>
// 引入响应式及计算属性相关依赖
import { reactive, computed } from 'vue'
// 创建一个响应式对象
const author = reactive({
    name: '张三',
    books: [
        { title: '书籍1', price: 100 },
        { title: '书籍2', price: 200 },
        { title: '书籍3', price: 300 }
    ]
})
// 创建一个计算属性对象
const publishedBooks = computed(() => {
    return author.books.length > 0 ? author.books : [{ title: '暂无书籍', price: 0 }]
})


</script>

<style scoped></style>
