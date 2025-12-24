<template>
  <article>
    <h3 class="text-2xl font-normal mb-4">{{ title }}</h3>
    <p class="font-mono text-neutral-400 mb-4">{{ description }}</p>
    <p class="font-mono mb-4">
      <span class="text-neutral-500">Стек: </span>{{ stack.join(", ") }}
    </p>
    <p class="font-mono">
      <span class="text-neutral-500">Мин. цена: </span>{{ minPrice }} ₽
    </p>
  </article>
</template>

<script setup lang="ts">
const { title, description, stack, minPrice } = defineProps<{
  title: string;
  description: string;
  stack: string[];
  minPrice: number;
}>();
</script>
