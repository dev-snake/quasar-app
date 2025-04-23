<template>
  <q-card class="col-5" flat>
    <q-item class="q-py-xs row q-gutter-xs bg-secondary shadow-custom-v2 q-mt-xs">
      <q-img
        src="/src/assets/images/store.png"
        class="rounded-borders"
        style="width: 60px; height: 60px"
      />
      <q-item-section class="q-pa-none">
        <div class="row items-center">
          <q-icon class="bx bx-store q-mr-xs text-grey text-caption" size="xs" tag="i"></q-icon>
          <span class="ellipsis text-caption">EV Store</span>
        </div>
        <span class="text-grey q-mt-xs font-xs">Garland, TX</span>
        <div class="row items-center q-mt-xs">
          <div class="row items-center">
            <q-icon name="star" color="amber" class="font-sm" />
            <span class="text-grey font-xs">(2)</span>
          </div>
        </div>
      </q-item-section>
    </q-item>
  </q-card>
</template>

<script setup lang="ts"></script>
