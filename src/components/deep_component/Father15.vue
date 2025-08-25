<template>
    <div>
        <!-- 定义子组件自定义事件的逻辑 -->
        <MyComponent15 @someEvent="handleSomeEvent" />
        <hr>
        <MyComponent15 @twoEvent="(msg) => (alert(msg))" />
    </div>
</template>

<script setup>
// 引入子组件
import MyComponent15 from './MyComponent15.vue'
// 处理逻辑
const handleSomeEvent = () => {
    alert('自定义事件被触发');
}


</script>

<style scoped></style>