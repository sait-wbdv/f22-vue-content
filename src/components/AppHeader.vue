<script setup>
defineProps({
  title: {
    type: String,
    default: "Generic Header",
  },
  description: {
    type: String,
    default: "This is the default description for this page",
  },
});
</script>
<template>
  <header class="flex h-60 flex-col items-center justify-center">
    <h1
      class="bg-gradient-to-br from-slate-900 to-emerald-500 bg-clip-text py-4 text-3xl font-extrabold text-transparent lg:text-5xl"
    >
      {{ title }}
    </h1>
    <p class="max-w-prose text-center text-slate-900">
      {{ description }}
    </p>
  </header>
</template>
