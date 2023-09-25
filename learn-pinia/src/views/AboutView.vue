<template>
  <div class="about">
    <h1>About</h1>
    <button
      class="counter-button"
      @click="storeCounter.increaseCount"
    > 
   {{ storeCounter.count }}
    </button>
  </div>
</template>

<script setup> 
import { useCounterStore } from '../stores/counter';

const storeCounter = useCounterStore();
</script>

<style> 
.counter-button { 
  font-size: 50px;
  border-radius: 5px;
  border: none;
  position: absolute;
  right: 400px;
  top: 424px;
}
</style>


