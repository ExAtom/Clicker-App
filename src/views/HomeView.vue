<script setup lang="ts">
import { ref } from "vue";
import ClickerCountLabel from "../components/ClickerCountLabel.vue";
import ClickerButton from "../components/ClickerButton.vue";

const count = ref(
  parseInt(localStorage.getItem("count")?.toString() || "") || 0
);

function increment() {
  count.value = parseInt(count.value.toString()) + 1;
  localStorage.setItem("count", count.value.toString());
}
</script>

<template>
  <main
    class="flex flex-col content-between justify-between h-screen select-none bg-slate-900"
  >
    <div class="flex content-center justify-center h-full">
      <ClickerCountLabel :count="count" class="self-center" />
    </div>
    <div class="flex items-stretch m-8">
      <ClickerButton @click="increment()" class="w-full" />
    </div>
  </main>
</template>
