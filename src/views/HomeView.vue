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
const arr = [
  {
    id: 1,
    img: {
      src: "src/assets/images/youtube.svg",
      alt: "Image",
    },
    text: "Thing one",
  },
  {
    id: 2,
    src: "src/assets/images/youtube.svg",
    text: "Thing Two",
  },
  {
    id: 3,
    src: "src/assets/images/youtube.svg",
    text: "Thing Three",
  },
  {
    id: 4,
    src: "src/assets/images/youtube.svg",
    text: "Thing Three",
  },
];
</script>

<template>
  <main>
    <AppHeader
      :title="info.label"
      :description="info.description"
    >
    </AppHeader>
    <section class="my-12 flex justify-around">
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
    <section class="my-12 flex justify-center">
      <ul>
        <!-- Attach v-for loop to the item that will be duplicated-->
        <li
          v-for="item in arr"
          :key="item.id"
        >
          <p>{{ item.id }}</p>
          <img
            :src="item.img.src"
            :alt="item.img.alt"
            class="w-12"
            v-if="item.img"
          />
          <img
            :src="item.src"
            v-else
          />
        </li>
      </ul>
    </section>
  </main>
</template>
