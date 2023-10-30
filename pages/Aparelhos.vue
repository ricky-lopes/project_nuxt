<template>
  <div>
    <div class="w-full flex gap-3 items-center">
      <h1 class="font-bold text-3xl">Aparelhos</h1>
      <button class="bg-red-600 text-white p-3 rounded-3xl hover:bg-white hover:text-red-600 hover:shadow-2xl" @click="showModal = true">Cadastrar</button>
    </div>
    <Modal v-show="showModal" @close-modal="showModal = false" title="Novo Aparelho">
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
            Nome: 'Remada',
            Manutenção: '20/12/2024',
            Máxima: '200kg'
        },
        {
            id: 2,
            Nome: 'Abdutor',
            Manutenção: '20/12/2024',
            Máxima: '200kg'
        }, 
        {
            id: 3,
            Nome: 'Crossover',
            Manutenção: '20/12/2024',
            Máxima: '200kg'
        }, 
        {
            id: 4,
            Nome: 'Puxador',
            Manutenção: '20/12/2024',
            Máxima: '200kg'
        }, 
        {
            id: 5,
            Nome: 'Voador',
            Manutenção: '20/12/2024',
            Máxima: '200kg'
        }, 
        {
            id: 6,
            Nome: 'Flexora',
            Manutenção: '20/12/2024',
            Máxima: '200kg'
        }
      ]
    }
  },
}
</script>

<style>
</style>