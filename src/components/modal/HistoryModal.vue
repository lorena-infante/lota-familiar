<template>
  <button class="btn-tertiary" @click="showModal = true">
    {{textButton}}
  </button>
  <transition name="fade" appear>
    <div class="modal-overlay" v-if="showModal" @click="showModal = false" />
  </transition>
  <transition name="slide" appear>
  <div class="modal" v-if="showModal">
    <div class="header">
      <h1>{{title}}</h1>
    </div>
    <div class="line" />
    <div class="body">
      <ul> soy una ul
        <li>soy un li</li>
      </ul>
    </div>
    <div class="footer">
      <button class="close" @click="showModal = false">{{closeText}}</button>
    </div>
  </div>
  </transition>
</template>

<script>
export default {
  data(){
    return {
      title:'Historial de Números',
      closeText: 'Cerrar',
      showModal: true,
      textButton: 'Ver Historial'
    };
  },
  props: [],
}
</script>

<style scoped>
.btn-tertiary {
  border-color: var(--tertiary);
  color: var(--tertiary);
  border: 1px solid var(--tertiary);
}
.btn-tertiary:hover {
  background-color:var(--tertiary);
  color: var(--white);
}
.modal-overlay {
 position: absolute;
 top: 0;
 left: 0;
 right: 0;
 bottom: 0;
 z-index: 98;
 background-color: rgba(0, 0, 0, 0.3);
}
/* .modal {
  background-color: coral;
  border-radius: 15px;
  padding:20px;
  margin:12px;
} */
/* ver https://codepen.io/Tyler_Potts_/pen/PowdPRQ?editors=1100 */
.line {
  border:2px solid var(--dark);
}
</style>