<template>
    <div>
        <!-- 数据 -->
        <h4>{{ title }}</h4>
        <!-- 事件 -->
        <button @click="$emit('enlarge-text')">放大文字</button>
        <button @click="$emit('shrink-text')">缩小文字</button>
        <!-- 插槽 -->
        <slot></slot>
    </div>
</template>

<script setup>
// 在该(子)组件中定义title属性
defineProps(['title'])
// 在该(子)组件中定义自定义事件
defineEmits(['enlarge-text', 'shrink-text'])

</script>

<style lang="scss" scoped></style>