<template>
  <q-card class="no-shadow q-mb-md" bordered>
    <div class="overflow-hidden bg-white">
      <div class="row items-center q-mb-sm q-px-md q-pt-md">
        <div class="text-subtitle2">Featured categories</div>
        <q-space />
        <q-icon name="arrow_forward" size="xs" />
      </div>

      <horizontal-scroll ref-key="featureCategoriesScroll" class="q-px-md q-pb-md">
        <div
          v-for="(category, index) in categories"
          :key="index"
          class="text-center col-2"
          style="max-width: 60px"
        >
          <q-img
            src="/src/assets/images/logo2.png"
            spinner-color="primary"
            fit="cover"
            style="border-radius: 50%; height: 60px; width: 60px; border: 1px solid #eee"
          />
          <span class="q-mt-sm" style="font-size: 10px; width: 60px">
            {{ category.name }}
          </span>
        </div>
      </horizontal-scroll>
    </div>
  </q-card>
</template>

<script setup lang="ts">
import HorizontalScroll from './HorizontalScroll.vue';

interface Category {
  name: string;
  image: string;
}

defineProps<{
  categories: Category[];
}>();
</script>
