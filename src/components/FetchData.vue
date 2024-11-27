<script setup>
// import { ref } from "vue";
// let details = ref([]);
// async function getData() {
//   const posts = await fetch("https://jsonplaceholder.typicode.com/posts")
//   .then((res) => res.json())
//   .then((json)=>
//   details.value=json
//   )
  
// }
</script>

<template>
  
  
  <!-- <div>{{ details }}</div> -->
  <div class="card"> 
    <slot></slot>
  </div>
</template>

<style>
.card{
    width: 200px;
    height: 300px;
    border: 1px solid red;
}
</style>
