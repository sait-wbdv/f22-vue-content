<script setup>
import AppCard from "../components/AppCard.vue";
import AppButton from "../components/AppButton.vue";
const name = "augustus";

function strCapitalize(str) {
  return str[0] != str[0].toUpperCase()
    ? str[0].toUpperCase() + str.slice(1)
    : str;
}

function textColor(str) {
  return str[0] != str[0].toUpperCase() ? "text-red-500" : "text-green-500";
}
</script>

<template>
  <main>
    <header class="flex h-60 flex-col items-center justify-center">
      <h1
        class="bg-gradient-to-br from-slate-900 to-emerald-500 bg-clip-text py-4 text-3xl font-extrabold text-transparent lg:text-5xl"
      >
        Home Page
      </h1>
    </header>
    <section class="flex justify-around">
      <AppButton text="Push me" bgColor="bg-blue-500" />
      <AppButton text="High Five" bgColor="bg-red-500" />
      <AppButton text="Low Five" bgColor="bg-emerald-500" />
    </section>
    <section>
      <AppCard />
    </section>
  </main>
</template>
