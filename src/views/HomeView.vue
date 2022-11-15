<script setup>
const name = "augustus";

const strCapitalize = (str) => {
  return str[0] != str[0].toUpperCase()
    ? str[0].toUpperCase() + str.slice(1)
    : str;
};

const textColor = (str) => {
  return str[0] != str[0].toUpperCase() ? "text-red-500" : "text-green-500";
};
</script>

<template>
  <main>
    <header class="flex h-60 flex-col items-center justify-center">
      <h1
        class="bg-gradient-to-br from-slate-900 to-emerald-500 bg-clip-text py-4 text-2xl font-extrabold text-transparent lg:text-5xl"
      >
        Home Page
      </h1>
    </header>
    <section
      class="container mx-8 mb-12 max-w-xl rounded-lg bg-slate-100 p-4 shadow-sm shadow-slate-900 lg:shadow-lg"
    >
      <header class="my-4">
        <h2 class="text-2xl font-semibold text-slate-900 lg:text-5xl">
          November 15 Examples
        </h2>
      </header>
      <div class="py-2">
        <h3 class="font-semibold">Render a Capitalized Name</h3>
        <p class="max-w-prose">
          In this example. The name is being capitalized using the function
          strCapitalize(), and the text color is defined using a ternary
          operatory in the paragraph tag's class binding
        </p>
        <div class="my-4">
          <p :class="textColor(name)" class="pb-2 text-xl lg:text-3xl">
            {{ name }}
          </p>
          <p
            :class="textColor(strCapitalize(name))"
            class="pb-2 text-xl lg:text-3xl"
          >
            {{ strCapitalize(name) }}
          </p>
        </div>
        <p class="max-w-prose text-sm text-slate-700">
          <em
            >By taking the reused ternary logic from the two paragraph tags to
            determine color and making them a function, the template code is
            much cleaner.</em
          >
        </p>
      </div>
    </section>
  </main>
</template>
