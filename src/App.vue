<script setup>
// 导入组件
import MyComponent01 from './components/MyComponet01.vue'
import MyComponent02 from './components/MyComponet02.vue'
import MyComponent03 from './components/MyComponet03.vue'
import MyComponent04 from './components/MyComponet04.vue'
import MyComponent05 from './components/MyComponet05.vue'

</script>

<template>
  <!-- 1.ref的使用 -->
  <!-- <MyComponent01 /> -->

  <!-- 2.reactive的使用 -->
  <!-- <MyComponent02 /> -->

  <!-- 3.测试computed计算属性 -->
  <!-- <MyComponent03 /> -->

  <!-- 4.测试条件渲染 -->
  <!-- <MyComponent04 /> -->

  <!-- 5.测试列表渲染 -->
  <MyComponent05 />

</template>

<style scoped></style>
