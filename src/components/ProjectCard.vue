<template>
  <article>
    <h3 class="text-2xl font-normal mb-4">{{ title }}</h3>
    <p class="font-mono text-neutral-400 mb-4">{{ description }}</p>
    <p class="font-mono mb-4">
      <span class="text-neutral-500">Стек: </span>{{ stack.join(", ") }}
    </p>
    <a v-if="link" :href="link" target="_blank" class="underline">> Перейти к проекту</a>
    <p v-else class="text-neutral-600">× Проект приватный</p>
  </article>
</template>

<script setup lang='ts'>
const { title, description, stack, link } = defineProps<{
  title: string;
  description: string;
  stack: string[];
  link?: string
}>();
</script>