<script setup lang="ts">
const emit = defineEmits(["click"]);
</script>

<template class="bg-red-500">
  <main
    class="bg-blue-600 rounded-2xl text-slate-100 font-bold p-5 text-center text-4xl shadow-xl shadow-blue-500/25 active:bg-blue-500 ease-out duration-100"
    @click="emit('click')"
  >
    Click
  </main>
</template>
