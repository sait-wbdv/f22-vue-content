<script setup>
defineProps({
  keyItem: {
    type: String,
    default: "Key",
  },
  valueItem: {
    type: String,
    default: "value",
  },
});
</script>
<template>
  <li>
    <span class="font-bold">{{ keyItem }}</span>
    <span class="text-gray-500">{{ valueItem }}</span>
  </li>
</template>
