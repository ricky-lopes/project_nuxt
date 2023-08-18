<template>
  <div>
    <div class="w-full flex gap-3 items-center">
      <h1 class="font-bold text-3xl">Alunos</h1>
      <button @click="showModal = true">Cadastrar Novo</button>
    </div>
    <Modal v-show="showModal" @close-modal="showModal = false" />

    <!-- <div class="save-btn">
      <button @click="showModal = true">Save</button>
    </div> -->
  </div>

</template>

<script>
import Modal from '~/components/Modal.vue'

export default {
  components: { Modal },
  data() {
    return {
      showModal: false,
    }
  },
}
</script>

<style>
button {
  background-color: #000;
  width: 150px;
  height: 40px;
  color: white;
  font-size: 14px;
  border-radius: 16px;

  &:hover {
    background-color: white;
    color: #000;
    border: 1px solid #000;
  }
}
</style>