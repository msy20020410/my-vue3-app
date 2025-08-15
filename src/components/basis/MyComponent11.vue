<template>
    <div class="my-component">

    </div>
</template>

<script setup>
// 引入生命周期钩子函数
import { onMounted } from 'vue'

// 执行在挂载后的自定义逻辑
onMounted(() => {
    alert('MyComponent11 组件已挂载')
})

</script>

<style scoped></style>