<script setup>
import Header from './components/Header.vue'
import Table from './components/Table.vue'
import Filtres from './components/Filtres.vue'
import ModalAddVisiter from './components/ModalAddVisiter.vue'
import { ref } from 'vue'
import { provide } from 'vue'
const ModalOpen = ref(false)
const OpenModal = () => {
  ModalOpen.value = true
}
const CloseModal = () => {
  ModalOpen.value = false
}
provide('ModalAction', {
  CloseModal,
  OpenModal,
})
</script>
<template>
  <div>
    <Header @open-modal="OpenModal" />
    <Table />
    <Filtres />
    <ModalAddVisiter v-if="ModalOpen" @close-modal="CloseModal" />
  </div>
</template>
