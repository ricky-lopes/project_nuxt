<template>
  <div class="modal-overlay" @click="$emit('close-modal')">
    <div class="modal" @click.stop>
        <div class="flex justify-between items-center">
            <h2 class="font-bold">Novo Aluno</h2>
            <div class="close" @click="$emit('close-modal')">
                <button class="close-img">
                  <h2 class="font-bold bg-green-600 px-1 rounded hover:bg-white hover:text-green-600">X</h2>
                </button>
            </div>
        </div>
        <form action="https://formeezy.com/api/v1/forms/64de9513a8e5560008bc2896/submissions" method="POST" enctype="multipart/form-data">
          <div class="flex flex-col mt-32">
            <UFormGroup label="Nome" required>
            <UInput placeholder="Fulano da silva..." icon="i-heroicons-user" /></UFormGroup>

            <UFormGroup label="Email" required>
            <UInput placeholder="you@example.com" icon="i-heroicons-envelope" /></UFormGroup>

            <UFormGroup label="Idade" required>
            <UInput placeholder="Apenas números" type="number" icon="i-heroicons-user" /></UFormGroup>

            <div class="flex justify-center w-full">
              <button class="mt-32 bg-green-600 font-bold px-1 rounded hover:bg-white hover:text-green-600" type="submit">Send</button>

            </div>
          </div>
            
        </form>
    </div>
  </div>
</template>
  
  <script>
    export default {
  }
  </script>

<style scoped>

.mt-32 {
  margin-top: 32px;
}

.modal-overlay {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 999;
  display: flex;
  justify-content: center;
  background-color: #000000da;
}

.modal {
  text-align: center;
  background-color: white;
  width: 500px;
  height: 350px;
  margin-top: 10%;
  padding: 24px;
  border-radius: 20px;
}
.close {
  cursor: pointer;
}

.check {
  width: 150px;
}

h6 {
  font-weight: 500;
  font-size: 28px;
  margin: 20px 0;
}

p {
  font-size: 16px;
  margin: 20px 0;
}

button {
  /* background-color: #ac003e; */
  padding: 4px 16px;
  /* height: 40px; */
  color: white;
  font-size: 14px;
  border-radius: 16px;
}
</style>