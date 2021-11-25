<template>
  <div id="app">
    <button @click="showModal = true" >Show modal</button>
    <Modal :showModal="showModal" @close-modal="showModal = false"></Modal>
  </div>
</template>

<script>
import Modal from "./components/Modal.vue"


export default {
  name: "App",
  data() {
    return {
      showModal: false
    };
  },
  components: {
    Modal
  },
};
</script>

<style>
#app {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 30px;
}
</style>
