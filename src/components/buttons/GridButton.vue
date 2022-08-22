<template>
<div class="grid">
  <!-- <button class="none">X</button> -->
  <button-item
    v-for="square in squares"
      :key="square.id"
      :number="square">
  </button-item>
</div>
  
</template>

<script>
import ButtonItem from './ButtonItem.vue';
export default {
  data(){
    return {
      squares: 90,
    }
  },
  components: {
    ButtonItem,
  },
  
}
</script>

<style scoped>
  .grid {
  display: grid;
  grid-template-rows: repeat(10, 2fr);
  grid-template-columns: repeat(9, 2fr);
  grid-auto-flow: column;
  }
  .none {
  background-color: var(--red);
  color: var(--white);
  padding: 20px;
  border-radius: 12px;
  cursor: default;
}

@media (max-width:768px) {
  .grid {
    display: grid;
    grid-template-rows: repeat(10, 1fr);
    grid-template-columns: repeat(1, 1fr);
    grid-auto-flow: column;
  }
}
</style>