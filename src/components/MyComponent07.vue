<template>
    <div class="my-component07">
        <!-- 单行文本输入 -->
        <p>你输入的内容是:</p>
        {{ msg }}
        <input type="text" v-model="msg" placeholder="请输入内容" />
        <hr>
        <!-- 多行文本输入 -->
        <p style="white-space: pre-line;">你输入的内容是: {{ multilineText }}</p>
        <textarea v-model="multilineText" placeholder="请输入内容"></textarea>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const msg = ref('')

const multilineText = ref('')


</script>

<style scoped></style>