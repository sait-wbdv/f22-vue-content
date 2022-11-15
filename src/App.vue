<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header
    class="flex items-center justify-between bg-gradient-to-r from-violet-500 via-emerald-500 to-emerald-700 p-4 md:p-8"
  >
    <div class="flex items-center gap-4">
      <img
        alt="Vue logo"
        class="logo"
        src="@/assets/images/logo.svg"
        width="64"
        height="64"
      />
      <p class="text-3xl font-bold text-slate-700">Lilyx</p>
    </div>
    <nav>
      <ul class="flex gap-4">
        <li>
          <RouterLink to="/" class="text-xl font-semibold text-slate-50"
            >Home</RouterLink
          >
        </li>
        <li>
          <RouterLink to="/about" class="text-xl font-semibold text-slate-50"
            >About</RouterLink
          >
        </li>
      </ul>
    </nav>
  </header>
  <!-- RouterView shows the content from your pages or "views" -->
  <RouterView />

  <footer class="grid h-20 place-items-center bg-slate-700 text-white">
    <p>&copy; 2022 Ashlyn Knox</p>
  </footer>
</template>
