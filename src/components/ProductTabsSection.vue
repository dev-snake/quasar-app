<template>
  <q-card class="no-shadow q-pb-md q-pt-md q-px-md bg-white">
    <div>
      <div class="row items-center q-gutter-x-md">
        <span class="text-underline">All</span>
        <tab-item icon="auto_awesome" label="New" />
        <tab-item icon="emoji_events" label="Best" />
        <tab-item icon="bolt" label="Deals" />
      </div>
      <div class="row q-mt-md">
        <product-card class="col-6" v-for="i in 4" :key="i" />
      </div>
    </div>
  </q-card>
</template>

<script setup lang="ts">
import ProductCard from './ProductCard.vue';
import TabItem from './TabItem.vue';
</script>
