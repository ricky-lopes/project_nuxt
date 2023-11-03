<template>
  <div class="modal-overlay" @click="$emit('close-modal')">
    <div class="modal" @click.stop>
        <div class="flex justify-between items-center mb-6">
            <h2 class="font-bold">{{ title }}</h2>
            <div class="cursor-pointer" @click="$emit('close-modal')">
                <button class="close-img">
                  <h2 class="font-bold text-white bg-red-600 px-1 rounded hover:bg-white hover:text-red-600">X</h2>
                </button>
            </div>
        </div>
        <slot></slot>
    </div>
  </div>
</template>
  
  <script>
    export default {
      props:['title']
  }
  </script>

<style scoped>

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
  height: fit-content;
  margin-top: 10%;
  padding: 24px;
  border-radius: 20px;
}
</style>