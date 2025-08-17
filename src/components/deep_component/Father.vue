<template>
    <div>
        <!-- 引入子组件,并进行事件的调用 -->
        <MyComponent13 @my-event="handleMyEvent" @get-time="handleGetTime" />



    </div>
</template>

<script setup>
// 引入13号子组件
import MyComponent13 from './MyComponent13.vue'

function handleMyEvent() {
    alert('你好自定义事件!')
}

function handleGetTime(time) {
    alert('当前时间: ' + time)
}

</script>

<style scoped></style>