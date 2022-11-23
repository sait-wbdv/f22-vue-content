<script setup>
defineProps({
  text: String,
});
</script>
<template>
  <li class="max-w-prose py-2">
    {{ text }}
  </li>
</template>
