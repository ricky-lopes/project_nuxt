<template>
  <div>
    <div class="w-full flex gap-3 items-center">
      <h1 class="font-bold text-3xl">Alunos</h1>
      <button class="btn-primary" @click="showModal = true">Cadastrar</button>
    </div>
    <Modal v-show="showModal" @close-modal="showModal = false" title="Novo Aluno">
      <form action="https://formeezy.com/api/v1/forms/64de9513a8e5560008bc2896/submissions" method="POST" enctype="multipart/form-data">
          <div class="flex flex-col">
            <UFormGroup label="Nome" required>
            <UInput placeholder="Fulano da silva..." icon="i-heroicons-user" /></UFormGroup>

            <UFormGroup label="Email" required>
            <UInput placeholder="you@example.com" icon="i-heroicons-envelope" /></UFormGroup>

            <UFormGroup label="Idade" required>
            <UInput placeholder="Apenas números" type="number" icon="i-heroicons-user" /></UFormGroup>

            <div class="flex justify-center w-full">
              <button class="mt-12 bg-red-600 font-bold px-1 rounded hover:bg-white hover:text-red-600" type="submit">Send</button>
            </div>
          </div>
        </form>
    </Modal>

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