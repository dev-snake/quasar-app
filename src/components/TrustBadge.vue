<template>
  <div class="row q-mb-lg">
    <div class="col-1">
      <q-icon :name="icon" color="green" size="sm" />
    </div>
    <div class="col-10">
      <div class="text-weight-medium">{{ title }}</div>
      <div class="q-mb-xs text-grey-7 q-mt-xs font-xs" >
        {{ description }}
      </div>
      <slot></slot>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  icon: string;
  title: string;
  description: string;
}>();
</script>
