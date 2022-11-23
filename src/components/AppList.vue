<script setup>
defineProps({
  list: {
    type: [Array, Object],
  },
});
</script>
<template>
  <div
    class="container my-4 mx-4 max-w-lg md:mx-12"
    v-if="list != ''"
  >
    <ul
      v-if="list"
      class="p-4"
    >
      <!-- list item component: handles the styles of each list item -->
      <li
        v-for="listItem in list"
        :key="listItem.id"
      >
        {{ listItem }}
      </li>
    </ul>
    <!-- if no list is passed, use this component like a generic html component-->
    <ul
      v-else
      class="p-4"
    >
      <slot></slot>
    </ul>
  </div>
</template>
