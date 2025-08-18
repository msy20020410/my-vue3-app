<template>
    <div>
        <!-- 引入14号子组件,并传递一个自定义的属性 -->
        <!-- <MyComponent14 v-model="customModel" v-model:title="customTitle"  /> -->

        <!-- 该父组件传递数据,并展示数据 -->
        <MyComponent14 v-model:man="man" v-model:pwd="pwd" />
        <div>子组件将man修改为了:{{ man }}</div>
        <div>子组件将pwd修改为了:{{ pwd }}</div>

    </div>
</template>

<script setup>

import MyComponent14 from './MyComponent14.vue'
import { ref } from 'vue';

const customModel = ref('Hello World');
const customTitle = ref('你好,参数!')

// 定义用户名和密码
const man = ref('张三');
const pwd = ref('123');


</script>

<style scoped></style>