<template>
  <div class="modal-overlay" @click="$emit('close-modal')">
    <div class="modal" @click.stop>
        <div class="flex justify-between items-center">
            <h2 class="font-bold">Novo Cliente</h2>
            <div class="close" @click="$emit('close-modal')">
                <button class="close-img">X</button>
            </div>
        </div>
        <form class="flex-col mt-32" action="https://formeezy.com/api/v1/forms/64de9513a8e5560008bc2896/submissions" method="POST" enctype="multipart/form-data">
            <div class="flex-col">
                <input type="email" name="email" placeholder="Enter email" required/>
                <button type="submit">Send</button>
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
  display: flex;
  justify-content: center;
  background-color: #000000da;
}

.modal {
  text-align: center;
  background-color: white;
  width: 500px;
  height: 300px;
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
  background-color: #ac003e;
  padding: 4px 16px;
  /* height: 40px; */
  color: white;
  font-size: 14px;
  border-radius: 16px;
}
</style>