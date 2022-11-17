<script setup>
import AppCard from "../components/AppCard.vue";
import AppButton from "../components/AppButton.vue";
import AppHeader from "../components/AppHeader.vue";
// JS Variable for youtube
const info = {
  title: "Welcome to the Home Page",
  description:
    "This website is for documenting the things that we learn to do in VueJS.",
};
const youtube = {
  src: "src/assets/images/youtube.svg",
  alt: "Youtube Logo",
};
</script>

<template>
  <main>
    <AppHeader
      :title="info.title"
      :description="info.description"
    />
    <section class="flex justify-around">
      <AppButton
        text="Push me"
        bgColor="bg-blue-500"
        src="src/assets/images/logo.svg"
      />
      <AppButton
        text="High Five"
        bgColor="bg-red-500"
        num="5"
        :src="youtube.src"
        :altText="youtube.alt"
      />
      <AppButton
        text="Low Five"
        bgColor="bg-emerald-500"
        altText="Nothing"
      />
    </section>
    <section>
      <AppCard />
    </section>
  </main>
</template>
