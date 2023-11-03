<template>
  <div>
    <div class="w-full flex gap-3 items-center">
      <h1 class="font-bold text-3xl">Treinos</h1>
      <button class="btn-primary" @click="showModal = true">Cadastrar</button>
    </div>
    <Modal v-show="showModal" @close-modal="showModal = false" title="Novo Treino">
      <form action="https://formeezy.com/api/v1/forms/64de9513a8e5560008bc2896/submissions" method="POST" enctype="multipart/form-data">
          <div class="flex flex-col">
            <UFormGroup label="Aluno" required>
            <USelect  placeholder="Fulano da Silva..." :options="data" icon="i-heroicons-user" option-attribute="name"/></UFormGroup>

            <UFormGroup label="Aparelho" required>
            <USelect placeholder="Voador" :options="equipment" icon="i-heroicons-cog-6-tooth-20-solid" option-attribute="name"/></UFormGroup>

            <UFormGroup label="Exercício" required>
            <USelect placeholder="Remada Alta" :options="training" icon="i-heroicons-heart" option-attribute="name"/></UFormGroup>

            <UFormGroup label="Repetições" required>
            <UInput placeholder="3x12" icon="i-heroicons-arrow-path" option-attribute="name"/></UFormGroup>

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

const people = [
  {
    name: 'Fulano de lá',
    value: 'CA',
  },
  {
    name: 'Dagoberto Roberto',
    value: 'EUA',
  },
  {
    name: 'Rubens Robson da Silva',
    value: 'BR',
  }
]

const equipment = [
  {
    name: 'Voador',
    value: 'CA',
  },
  {
    name: 'Flexora',
    value: 'EUA',
  },
  {
    name: 'Crossover',
    value: 'BR',
  }
]

const training = [
  {
    name: 'Remada Alta',
    value: 'CA',
  },
  {
    name: 'Rosca Alternada',
    value: 'EUA',
  },
  {
    name: 'Levantamento Lateral',
    value: 'BR',
  }
]

export default {
  components: { Modal },
  data() {
    return {
      showModal: false,
      peoples : [
        {
            id: 1,
            Aluno: 'Ricky',
            Aparelho: 'Remada',
            Exercício: 'Remada Alta',
            Repetições: '3x15',
            Carga: '200kg'
        },
        {
            id: 2,
            Aluno: 'Ricky',
            Aparelho: 'Remada',
            Exercício: 'Remada Alta',
            Repetições: '3x15',
            Carga: '200kg'
        }, 
        {
            id: 3,
            Aluno: 'Ricky',
            Aparelho: 'Remada',
            Exercício: 'Remada Alta',
            Repetições: '3x15',
            Carga: '200kg'
        }, 
        {
            id: 4,
            Aluno: 'Ricky',
            Aparelho: 'Remada',
            Exercício: 'Remada Alta',
            Repetições: '3x15',
            Carga: '200kg'
        }, 
        {
            id: 5,
            Aluno: 'Ricky',
            Aparelho: 'Remada',
            Exercício: 'Remada Alta',
            Repetições: '3x15',
            Carga: '200kg'
        }, 
        {
            id: 6,
            Aluno: 'Ricky',
            Aparelho: 'Remada',
            Exercício: 'Remada Alta',
            Repetições: '3x15',
            Carga: '200kg'
        }
      ],
      data: people,
      equipment: equipment,
      training: training
    }
  },
}
</script>

<style>
</style>