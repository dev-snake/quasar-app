<template>
  <q-card class="no-shadow bg-white q-mb-md" bordered>
    <div class="row items-center q-mb-sm q-px-md q-pt-md">
      <div class="text-subtitle2">Hot brands</div>
      <q-space />
      <q-icon name="arrow_forward" size="xs" />
    </div>
    <horizontal-scroll ref-key="hotBrandsScroll" class="q-px-md q-pb-md">
      <div v-for="(brand, index) in brands" :key="index" class="text-center">
        <q-card class="no-shadow bg-white" style="border: 1px solid #eee">
          <q-img
            src="/src/assets/images/hot_branch.png"
            spinner-color="primary"
            height="60px"
            fit="cover"
            style="height: 60px; width: 60px"
          />
        </q-card>
        <span style="font-size: 10px; width: 60px">
          {{ brand.name }}
        </span>
      </div>
    </horizontal-scroll>
  </q-card>
</template>

<script setup lang="ts">
import HorizontalScroll from './HorizontalScroll.vue';

interface Brand {
  name: string;
  logo: string;
}

defineProps<{
  brands: Brand[];
}>();
</script>
