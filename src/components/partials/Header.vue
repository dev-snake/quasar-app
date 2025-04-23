<template>
  <q-header class="q-mx-auto bg-white q-py-xs no-shadow" style="max-width: 420px">
    <div class="row justify-between items-center q-pl-xs q-pr-xs">
      <q-icon tag="i" class="bx bx-heart text-black text-h5" />
      <h1 class="text-black text-h6" style="font-weight: 600">Marketplace</h1>
      <q-icon tag="i" class="bx bx-cart-alt text-black text-h5" />
    </div>
    <div class="relative-position q-px-xs">
      <input type="text" class="w-full input-search" />
      <q-icon
        tag="i"
        class="bx bx-search text-black absolute"
        style="top: 50%; transform: translate(1rem, -50%); left: 0"
      />
    </div>
  </q-header>
</template>

<script setup lang="ts"></script>

<style scoped>
.input-search {
  background: #eee;
  border: none;
  outline: none;
  padding: 6px 2rem 0.5rem;
  border-radius: 2rem;
}
</style>
