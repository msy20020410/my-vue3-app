<template>
  <div>
    <div>{{ model }}</div>
    <div>{{ title }}</div>
    <hr>
    <!-- 输入用户名和密码 -->
    <input type="text" v-model="man" placeholder="请输入用户名">
    <br>
    <input type="text" v-model="pwd" placeholder="请输入密码">

  </div>
</template>

<script setup>

// 在该子组件中,定义一个属性绑定
import { defineModel } from 'vue';
const model = defineModel();
// 定义一个带参数的属性绑定
const title = defineModel('title')

// 定义用户名和密码属性
const man = defineModel('man')
const pwd = defineModel('pwd')

</script>

<style lang="scss" scoped></style>