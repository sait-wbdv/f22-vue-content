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
    <span class="font-bold">{{ keyItem }}</span> <span>{{ valueItem }}</span>
  </li>
</template>
