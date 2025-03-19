<script setup>
import { inject, ref } from 'vue'
const { CloseModal } = inject(['ModalAction'])
</script>
<template>
  <div class="DrawerModal">
    <div class="ModalAdd">
      <input placeholder="Имя" />
      <input placeholder="Группа" />
      <input placeholder="Компания" />
      <button>Dobavit</button>
      <button @click="CloseModal()">Закрыть</button>
    </div>
  </div>
</template>
<style scoped>
.ModalAdd {
  position: fixed;
  display: flex;
  flex-direction: column;
  background-color: aquamarine;
  left: 40vh;
  top: 40vh;
  width: 50vh;
  height: 30vh;
}
.DrawerModal {
  position: fixed;
  top: 0px;
  left: 0px;
  height: 100%;
  width: 100%;
  background-color: black;
  z-index: 10;
  opacity: 0.65;
}
</style>
