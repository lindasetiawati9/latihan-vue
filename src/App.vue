<script setup>
import { ref } from 'vue'

const msg = "Hello World"
const rawHtml ="<li>Teks Ini Berwarna Merah</li>"
let a=10
let b=5
let c=a+b
const link = "https://youtu.be/YT08A8Jucj0"
</script>

<template>
  <div v-bind="dynamicId" id="app">
    <h1>{{ msg }}</h1>

    <span style="color: red" v-html="rawHtml" ></span>
    <button :disabled="isButtonDisabled"><a :href="link"> Youtube </a></button> <br>
    Bilangan 1 = {{ a }}<br>
    Bilangan 2 = {{ b }}<br>
    Hasil = {{ c }}
  </div>
</template>