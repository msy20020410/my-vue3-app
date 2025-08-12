<template>
    <div class="my-component05">
        <!-- 遍历书籍列表 -->
        <ul>
            <li v-for="(book, index) in books" :key="book.id">
                {{ name }} - {{ index }} - {{ book.title }} - {{ book.author }}
            </li>
        </ul>
        <hr>
        <!-- 遍历一个对象的所有属性 -->
        <ul>
            <li v-for="(value, key, index) of person" :key="key">
                {{ index }} - {{ key }} - {{ value }}
            </li>
        </ul>
        <hr>
        <!-- 嵌套遍历 -->
        <ul v-for="number in numbers" :key="index">
            <li v-for="n in even(number)" :key="n">
                {{ n }}
            </li>
        </ul>
    </div>
</template>

<script setup>
import { reactive, ref } from 'vue'

const name = ref('书名')

// 创建书籍列表
const books = ref([
    { id: 1, title: 'Vue.js实战', author: '尤雨溪' },
    { id: 2, title: '深入浅出Vue.js', author: '李洪洋' },
    { id: 3, title: 'Vue.js权威指南', author: '黄轶' }
])

// 创建对象
const person = reactive({
    name: '张三',
    age: 30,
    address: '北京市'
})

// 创建二维数组对象
const numbers = ref([
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
])

// 创建一个对二维数组求偶数的函数
function even(numbers) {
    return numbers.filter(item => item % 2 === 0)
}





</script>

<style scoped></style>
