<script setup>
import AppHeader from "../components/AppHeader.vue";
const pageInfo = {
  title: "Our About Page",
  description: "Learn about our cool website",
};
</script>
<template>
  <main>
    <AppHeader :title="pageInfo.title" />
  </main>
</template>
