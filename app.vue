<template>
  <button
    @click="emitModalShow"
      class="pc-4 py-2 bg-blue-500 text-white hover:bg-blue-600"
  >Otwórz modal</button>

  <Modal @modalValue="emitModalShow" :modalValue="showModal" :nameuser="'Szymon Guzik'"/>
</template>
<script setup>
const showModal = ref(false)

const emitModalShow = () => {
  showModal.value = !showModal.value
}
</script>