<script setup>
import { ref } from "vue";
import Slots from "./components/Slots.vue";
import CardSlot from './components/CardSlot.vue'
import FetchData from "./components/FetchData.vue";
// let num = ref(20);
let details = ref([]);
async function getData() {
  const posts = await fetch("https://jsonplaceholder.typicode.com/posts")
  .then((res) => res.json())
  .then((json)=>
  details.value=json
  )
}
</script>

// Slots component template rendering
 <!-- <template>
  <h1>Parent Component : {{ num }}</h1>
  <Slots>
    <template v-slot:food="{ foodName }">
      <h3>{{ foodName }}</h3>
    </template>

    <template v-slot:btnSlot> Submit </template> -->

    
   <!--    
   </Slots>

   <Slots v-slot:localdata="dataFromSlot">{{ dataFromSlot.lclData }}</Slots>
</template> 
-->

//CardSlot component rendering
 <!-- <template>
<CardSlot>
</CardSlot>
</template>  -->

// FetchData component rendering
<!-- <template>
  <h1>FetchData</h1>
  <button @click="getData">Get Data</button>
<FetchData v-for="i in details" :key="i">
  <p>{{i}}</p>
 
</FetchData>
  
</template> -->

<style scoped>
h3 {
  background-color: aqua;
  color: red;
  width: 100px;
  font-size: larger;
  padding: 20px;
}
</style>
