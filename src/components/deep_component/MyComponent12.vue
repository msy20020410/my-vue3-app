<template>
  <div>
    {{ name }} - {{ age }}
    <hr>

  </div>
</template>

<script setup>
// 使用对象的形式定义props
defineProps({
  name: String,
  age: Number
})

</script>

<style lang="scss" scoped></style>