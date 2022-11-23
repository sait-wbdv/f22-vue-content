<script setup>
defineProps({
  list: {
    type: [Array, Object],
  },
});
</script>
<template>
  <div class="container my-4 mx-4 max-w-lg md:mx-12">
    <!-- Use this if an array is passed-->
    <ul
      v-if="list != ''"
      class="p-4"
    >
      <!-- A simple flat array would render easily here-->
      <li
        v-for="listItem in list"
        :key="listItem.id"
        class="max-w-prose py-2"
      >
        {{ listItem }}
      </li>
    </ul>
    <!-- Otherwise use this and manually controll content in a slot -->
    <ul
      v-else
      class="p-4"
    >
      <slot></slot>
    </ul>
  </div>
</template>
