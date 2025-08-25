<template>
  <div>
    <!-- 子组件展示当前值 -->
    <p>在组件当前值: {{ count }}</p>
    <button @click="increment">自增</button>
  </div>
</template>

<script setup>
// 定义模型值
const count = defineModel()

// 创建自增函数
const increment = () => {
  count.value++
}

</script>

<style lang="scss" scoped></style>