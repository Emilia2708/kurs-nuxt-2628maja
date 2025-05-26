<template>
  <div>
    <button class="inc" @click="increments">Drugi post {{ count }}</button>
    <button class="inc" @click="showHideUsers">Lista postów </button>

    <ul v-if="showuser">
      <li>1 post</li>
      <li>2 post</li>
      <li>3 post</li>
      <li>4 post</li>
    </ul>

  </div>
</template>

<script lang="ts" setup>
const count = ref(0)
const showuser = ref(false)

const increments = () => {
  count.value++
}

const showHideUsers = () => {
  showuser.value = !showuser.value
}

</script>

<style scoped>
.inc {
  padding: 10px 10px 10px;
  background-color: aqua;
  border: unset;
  cursor: pointer;
  font-size: 15px;
}
</style>