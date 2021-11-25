<template>
  <div class="modal" v-if="showModal">
    <div class="modal-block">
      <button type="button" @click="closeModal">Close</button>
    </div>
  </div>
</template>


<script type="text/javascript">
export default {
    props: ['showModal'],
    methods: {
        closeModal() {
            this.$emit('close-modal')
        }
    }
}
</script>


<style>
.modal {
  display: flex;
  justify-content: center;
  align-items: center;
  background: grey;
  width: 100%;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
}
.modal-block {
  width: 600px;
  background: white;
  height: 300px;
  border-radius: 4px;
  margin: 0 auto;
  padding: 10px;
  box-sizing: border-box;
}
.modal-block button {
  margin-left: auto;
  margin-right: 0;
  display: block;

}
</style>
