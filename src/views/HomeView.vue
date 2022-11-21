<script setup>
import AppCard from "../components/AppCard.vue";
import AppButton from "../components/AppButton.vue";
import AppHeader from "../components/AppHeader.vue";
// JS Variable for youtube
const info = {
  label: "Welcome to the Home Page",
  description:
    "This website is for documenting the things that we learn to do in VueJS.",
};
// const youtube = {
//   src: "src/assets/images/youtube.svg",
//   alt: "Youtube Logo",
// };
const buttons = [
  {
    text: "Push Me",
    bgColor: "bg-blue-500",
    src: "src/assets/images/logo.svg",
  },
  {
    text: "High Five",
    bgColor: "bg-red-500",
    src: "src/assets/images/youtube.svg",
  },
  {
    text: "Low FIve",
    bgColor: "bg-emerald-500",
  },
];
const arr = ["one", "two", "three", "four"];
</script>

<template>
  <main>
    <AppHeader
      :title="info.label"
      :description="info.description"
    >
    </AppHeader>
    <section class="flex justify-around">
      <AppButton
        v-for="thing in buttons"
        :key="thing.id"
        :text="thing.text"
        :bgColor="thing.bgColor"
      />
    </section>
    <section>
      <AppCard />
    </section>
    <section>
      <ul>
        <!-- Attach v-for loop to the item that will be duplicated-->
        <li
          v-for="item in arr"
          :key="item.id"
        >
          {{ item }}
        </li>
      </ul>
    </section>
  </main>
</template>
