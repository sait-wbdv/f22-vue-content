<script setup>
// Import Component
import AppList from "../components/AppList.vue";
import AppListItem from "../components/AppListItemKv.vue";
import AppLink from "../components/AppLink.vue";
// Page (or API) stores the information that goes into the list
const arr = [1, 2, 3, 4];
const lyrics = [
  { i: "Hello ", x: "By the Beatles" },
  { i: "Goodbye ", x: "Don't Sue me for Copyright" },
  { i: "You Say ", x: "Neato" },
  { i: "I Say ", x: "Goodbye" },
];
</script>
<template>
  <main>
    <AppLink url="https://github.com">Github</AppLink>
    <!-- Apply Component -->
    <!-- Pass information to it-->
    <AppList :list="arr" />
    <!-- Pass array of objects to a component-->
    <!-- Component iterates through objects -->
    <!-- Render each key-value pair without them needing the same keys -->
    <AppList>
      <AppListItem
        v-for="lyric in lyrics"
        :key="lyric.id"
        :keyItem="lyric.i"
        :valueItem="lyric.x"
      />
    </AppList>
  </main>
</template>
