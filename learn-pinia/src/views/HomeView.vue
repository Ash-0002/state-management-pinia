<template>
  <div class="home">
    <div class="count">
      {{ storeCounter.count }}
    </div>
    <div class="buttons">
      <button @click="storeCounter.decreaseCount">-</button>
      <button @click="storeCounter.increaseCount">+</button>
    </div>
  </div>
  <!-- <hr><br> -->
  <div class="oddEven">This Counter is : {{ storeCounter.oddOrEven }}</div>
  <br>
  <hr>
  <br>
  <div class="oddEven">Edit Counter: </div> 
   <input type="number" v-model="storeCounter.count">
</template>

<script setup> 
import { ref, computed } from 'vue';
import  { useCounterStore } from '@/stores/counter'

  const storeCounter = useCounterStore(); 
  // const count = ref(0); 

  // const increaseCount = () => { 
  //   console.log("increaseCount");
  //   count.value++; 
  // }
  // const decreaseCount = () => { 
  //   console.log("decreaseCount");
  //  count.value--;
  // }

  // const oddOrEven = computed(() => { 
  //   if (storeCounter.count % 2 === 0) return 'even';
  //   return 'odd';
  // })
</script>

<style>
  .home { 
    margin: 0 30px;
    align-items: center;
  }
  .count {
    font-size: 60px;
    display: flex;
    align-items: baseline;
    justify-content: space-around;
}
  .buttons { 
    padding: 10px;
  }

  .buttons > button {
    margin: 5px;
    padding: 5px 10px;
    border-radius: 5px;
    border: none;
  }
  
  .oddEven{ 
    text-align: center;
  }
</style>


