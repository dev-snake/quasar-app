<template>
  <div
    class="bg-white col-3 q-px-none shadow-1 rounded-borders"
    style="padding: 0 3px"
    v-for="i in 5"
    :key="i"
  >
    <div class="rounded-borders w-full">
      <q-img src="/src/assets/images/img1.png" class="w-full border-top-x" />
      <div class="text-negative q-pb-none q-px-xs">
        <span style="font-size: 12px">$</span
        ><strong style="display: inline-block; transform: translateY(4px); font-size: 16px"
          >9</strong
        ><span style="font-size: 12px">.90</span>
      </div>
      <div class="q-pt-none q-pb-xs q-px-xs row items-center justify-between">
        <span style="font-size: 10px; color: gray; text-decoration: line-through">14.00</span>
        <span class="bg-gradient-percent text-negative" style="font-size: 10px">14%</span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.bg-gradient-percent {
  background-image: linear-gradient(to right, #f8c7c7bd, #fadddd);
  padding: 0.1rem 0.4rem;
  border-radius: 8px;
}
</style>
