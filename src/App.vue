<template>
  <div>
    <header>
      <div class= "header">
      <h1>Lota Familiar</h1> 
      </div>
    </header>
    <form class="form-input">
      <div class="buttons">
      <button class="btn-delete">Limpiar Tablero</button>
      </div>
    </form>
    <section class="wrapper">
      <div class="grid">
        <grid-button />
      </div>
    </section>
  </div>
</template>

<script>
import './components/styles/styles.css';
import GridButton from './components/buttons/GridButton.vue';
export default {

  data() {
    return {
  }
},
  components: {
    GridButton,
  }
}
</script>

<style scoped>

.header {
  width: 100%;
  height: 5rem;
  background-color: var(--primary);
  color: var(--white);
  display: flex;
  justify-content: center;
  align-items: center;
}

.form-input {
  text-align: center;
  padding-top: 2%;
}
.label {
  display: block;
  font-size: 1.17em;
  font-weight: bold;
  color: var(--dark);
}

.btn-secondary {
 border-color: var(--secondary);
  color: var(--secondary);
  border: 1px solid var(--secondary);
}
.btn-secondary:hover {
  background-color: var(--secondary); 
  color: var(--white);
}

.btn-delete {
  border-color: 1px solid var(--red); 
  color: var(--red);
  border: 1px solid  var(--red);
}
.btn-delete:hover {
  background-color: var(--red); 
  color: var(--white);
}
.wrapper {
   text-align: center;
   padding: 2%;
}


@media (max-width:768px) {
  .wrapper {
    overflow-x: scroll;
  }
}
</style>