<script setup lang="ts">
defineProps({
  count: Number,
});
</script>

<template>
  <main class="text-8xl font-bold text-slate-200">
    {{ count }}
  </main>
</template>
