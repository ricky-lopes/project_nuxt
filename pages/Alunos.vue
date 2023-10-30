<template>
  <div>
    <div class="w-full flex gap-3 items-center">
      <h1 class="font-bold text-3xl">Alunos</h1>
      <button class="bg-red-600 text-white p-3 rounded-3xl hover:bg-white hover:text-red-600 hover:shadow-2xl" @click="showModal = true">Cadastrar</button>
    </div>
    <Modal v-show="showModal" @close-modal="showModal = false" />

    <!-- <div class="save-btn">
      <button @click="showModal = true">Save</button>
    </div> -->

    <div class="p-8">
      <Table :data="peoples" />
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
      peoples : [
        {
            id: 1,
            Nome: 'Ricky Walton',
            Idade: '20',
            email: 'lindsay.walton@example.com',
            role: 'Member'
        },
        {
            id: 2,
            Nome: 'Courtney Henry',
            Idade: '20',
            email: 'courtney.henry@example.com',
            role: 'Admin'
        }, 
        {
            id: 3,
            Nome: 'Tom Cook',
            Idade: '20',
            email: 'tom.cook@example.com',
            role: 'Member'
        }, 
        {
            id: 4,
            Nome: 'Whitney Francis',
            Idade: '20',
            email: 'whitney.francis@example.com',
            role: 'Admin'
        }, 
        {
            id: 5,
            Nome: 'Leonard Krasner',
            Idade: '20',
            email: 'leonard.krasner@example.com',
            role: 'Owner'
        }, 
        {
            id: 6,
            Nome: 'Floyd Miles',
            Idade: '20',
            email: 'floyd.miles@example.com',
            role: 'Member'
        }
      ]
    }
  },
}

 
</script>

<style>
</style>