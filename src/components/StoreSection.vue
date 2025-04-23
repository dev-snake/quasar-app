<template>
  <q-card class="q-my-md bg-white" bordered flat>
    <q-card class="bg-white no-shadow row justify-between items-center q-pa-md">
      <div class="row items-center">
        <q-icon class="bx bx-store q-mr-xs text-grey" size="xs" tag="i"></q-icon>
        <q-badge
          class="shipping-badge q-py-xs q-px-sm"
          color="pink-1"
          text-color="primary"
          align="middle"
          style="border-radius: 16px"
        >
          <q-icon name="local_shipping" class="q-mr-xs text-caption" />
          Ships from Nailzy
        </q-badge>
      </div>
      <div>
        <q-icon name="arrow_forward" size="xs" />
      </div>
    </q-card>
    <div class="bg-white rounded-borders">
      <div class="q-px-md">
        <horizontal-scroll ref-key="storeRowScroll" class="q-pb-md">
          <store-card v-for="i in 5" :key="i" />
        </horizontal-scroll>
      </div>
    </div>
  </q-card>
</template>

<script setup lang="ts">
import HorizontalScroll from './HorizontalScroll.vue';
import StoreCard from './StoreCard.vue';
</script>
