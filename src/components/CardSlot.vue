<script setup>
import { reactive } from 'vue';
let meals=reactive(['pizza','juice','laddu','puffs']);
</script>

<template>

<div v-for="(i,index) in meals" :key="index">
<h1>{{ i }}</h1>
<slot></slot>
</div>

</template>