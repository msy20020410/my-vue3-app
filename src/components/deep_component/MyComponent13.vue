<template>
  <div>

    <!-- 在该子组件中,自定义一个事件 @click="$emit('myEvent')" -->
    <button @click="$emit('myEvent')">触发自定义事件</button>
    <hr>
    <!-- 定义带参数的自定义事件 -->
    <button @click="$emit('getTime', new Date().toLocaleTimeString())">触发带参数的自定义事件</button>




  </div>
</template>

<script setup>


</script>

<style lang="scss" scoped></style>