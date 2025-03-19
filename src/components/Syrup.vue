
<template>
  <div class="syrup" :style="{ backgroundColor: currentSyrup }"></div>
  <button @click="changeColor">Change Color</button>
</template>


<script setup lang="ts">
import { useBeverageStore } from '../stores/beverage';


const { currentSyrup, setSyrupColor } = useBeverageStore();


const changeColor = () => {
  setSyrupColor('#ff6347'); // Example: Change to tomato red
};
</script>


<style lang="scss" scoped>
.syrup {
  transform: translateY(400%);
  position: relative;
  width: 100%;
  height: 20%;
  animation: pour-tea 2s 1s forwards;
  z-index: 2;
}
</style>

