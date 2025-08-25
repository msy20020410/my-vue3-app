<template>
    <!-- 普通插槽 -->
    <MyComponent17>{{ msg }}</MyComponent17>
    <hr>

    <!-- 具名插槽 -->
    <MyComponent17>
        <template v-slot="one">
            <div style="color: red;">这是第一个具名插槽的内容</div>
        </template>
        <template #two>
            <div style="color: green;">这是第二个具名插槽的内容</div>
        </template>
    </MyComponent17>
    <hr>
    <MyComponent17>
        <template v-slot="three">
            <div style="color: blue;">这是第三个具名插槽的内容</div>
        </template>
    </MyComponent17>
    <hr>
    <!-- 条件插槽 -->
    <MyComponent17>
        <div v-if="$slots" class="card-content">
            haha
        </div>
    </MyComponent17>

</template>

<script setup>
import MyComponent17 from './MyComponent17.vue'
const msg = 'Hello from Father17'


</script>

<style scoped></style>