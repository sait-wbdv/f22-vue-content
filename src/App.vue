<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header class="bg-gradient-to-r from-violet-500 via-emerald-500 to-emerald-700 flex  justify-between items-center p-4 md:p-8">
    <div class="flex gap-4 items-center">
      <img alt="Vue logo" class="logo" src="@/assets/images/logo.svg" width="64" height="64" />
      <p class="text-3xl font-bold text-slate-700">Lilyx</p>
    </div>
      <nav>
        <ul class="flex gap-4">
          <li>
           <RouterLink to="/" class="text-xl text-slate-50 font-semibold">Home</RouterLink>
          </li>
          <li>
           <RouterLink to="/about" class="text-xl text-slate-50 font-semibold">About</RouterLink>
          </li>
        </ul>
      </nav>
  </header>
  <!-- RouterView shows the content from your pages or "views" -->
  <RouterView />
  <footer class="grid place-items-center bg-slate-700 text-white h-20">
    <p>&copy; 2022 Ashlyn Knox</p>
  </footer>
</template>

