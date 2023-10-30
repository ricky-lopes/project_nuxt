<template>
  <div>
    <div class="w-full flex gap-3 items-center">
      <h1 class="font-bold text-3xl">Aparelhos</h1>
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