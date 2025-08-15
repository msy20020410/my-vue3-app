<template>
    <!-- 该组件为父组件 -->
    <div class="my-component10">
        <!-- 引入对计数器子组件的使用 -->
        <ButtonCounter />
        <hr>
        <!-- 引入对博客子组件的使用
             由于在BlogPost定义了title属性，这里可以使用该属性并传入title属性值
             (数据父传子)
        -->
        <BlogPost title="我的博客" />
        <hr>
        <!-- 使用v-for进行数据填充,使用子组件定义的事件,在该出调用,并编写逻辑 -->
        <BlogPost v-for="post in posts" :key="post.id" :title="post.title" :style="{ fontSize: size + 'em' }"
            @enlarge-text="size++" @shrink-text="shrinkText" />
        <hr>
        <!-- 向子组件的中间传递内容 -->
        <BlogPost>这是在子组件中的插槽内容</BlogPost>

    </div>
</template>

<script setup>
// 导入子组件
import ButtonCounter from './ButtonCounter.vue'
import BlogPost from './BlogPost.vue'
import { ref } from 'vue';

// 定义title数组
const posts = ref([
    { id: 1, title: '我的第一篇博客' },
    { id: 2, title: '我的第二篇博客' },
    { id: 3, title: '我的第三篇博客' }
])

// 定义调整字体的响应式数据
const size = ref(1)

// 定义缩放字体函数
function shrinkText() {
    size.value--
}




</script>

<style scoped></style>