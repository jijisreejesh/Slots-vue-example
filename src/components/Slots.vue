<script setup>
import { reactive } from "vue";
const foods = reactive(["Apple", "Mango", "Orange"]);
</script>
<template>
  <!-- By default -->
  <div class="child">
    <slot> </slot>
    <h2>Child Component</h2>
  </div>

  <button>
    <slot name="btnSlot">Save</slot>
    <!-- Named slot -->
  </button>

  <div>
    <slot v-bind:lclData="'It is local Data'" name="localdata"></slot>
    <!-- Scoped slot -->
  </div>
 
 <!--Slot props-->
 <div>
<slot name="propSlot" v-bind:propName="dataToSend"></slot>
</div>

  <!-- Scoped slot with array -->
  <slot v-for="i in foods" :key="i" :foodName="i" name="food"> </slot>

</template>



<style>
.child {
  border: 1px solid #ccc;
  padding: 10px;
}
</style>
