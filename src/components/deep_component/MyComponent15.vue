<template>
  <div>
    <!-- 定义自定义事件 -->
    <button @click="$emit('someEvent')">点击触发自定义事件</button>

  </div>
</template>

<script setup>

</script>

<style lang="scss" scoped></style>