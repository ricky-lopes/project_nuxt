<template>
  <div>
    <div class="w-full flex gap-3 items-center">
      <h1 class="font-bold text-3xl">Aparelhos</h1>
      <button class="btn-primary" @click="showModal = true">Cadastrar</button>
    </div>
    <Modal v-show="showModal" @close-modal="showModal = false" title="Novo Aparelho">
      <form action="https://formeezy.com/api/v1/forms/64de9513a8e5560008bc2896/submissions" method="POST" enctype="multipart/form-data">
          <div class="flex flex-col">
            <UFormGroup label="Nome" required>
            <UInput placeholder="Voador" icon="i-heroicons-cog-6-tooth-20-solid" /></UFormGroup>

            <UFormGroup label="Manutenção" required>
            <UInput placeholder="01/12/1999" icon="i-heroicons-calendar-days-solid" /></UFormGroup>

            <UFormGroup label="Carga Máxima" required>
            <UInput placeholder="200 Kg" type="number" icon="i-heroicons-hand-raised" /></UFormGroup>

            <div class="flex justify-center w-full">
              <button class="mt-12 text-white btn-primary" type="submit">Cadastrar</button>
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