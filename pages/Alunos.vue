<template>
  <div>
    <div class="w-full flex gap-3 items-center">
      <h1 class="font-bold text-3xl">Alunos</h1>
      <button class="bg-green-600 text-white p-3 rounded-3xl hover:bg-white hover:text-green-600 hover:shadow-2xl" @click="showModal = true">Cadastrar</button>
    </div>
    <Modal v-show="showModal" @close-modal="showModal = false" />

    <!-- <div class="save-btn">
      <button @click="showModal = true">Save</button>
    </div> -->

    <div class="p-8">
      <Table />
    </div>
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
</style>