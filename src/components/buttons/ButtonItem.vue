<template>
  <button 
    @click="setStatus"
    :class="[isSelected ? 'selectedClass' : 'square']">
    {{ number }}
  </button>
</template>

<script>
export default {
  props: ['number'],
  data(){
    return {
      isSelected: false,
      history:[],
      selectedValue: null,
    }
  },
  methods:{
    setStatus(){
      this.isSelected = !this.isSelected;
      if(this.isSelected){
        this.addSelectedValue();
      } else {
        this.removeSelectedValue();
      }
      
    },
    
    addSelectedValue(){
      this.selectedValue = this.number;
        console.log(this.selectedValue);
      
    },
    removeSelectedValue(){
      this.selectedValue = this.number;
      console.log('removed',this.selectedValue);
    },
  }
};
</script>

<style scoped>
.square {
  padding: 20px;
  background-color: var(--primary);
  margin: 3px;
  color: var(--white);
  border-radius: 12px;
}

.square:hover, .selectedClass {
  cursor: pointer;
  padding: 20px;
  margin: 3px;
  background-color: var(--red);
  color: var(--white);
  border-radius: 12px;
}
</style>