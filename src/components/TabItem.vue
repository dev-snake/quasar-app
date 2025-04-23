<template>
  <span>
    <q-icon :name="icon" color="grey-10" size="xs" class="q-mr-xs" />
    {{ label }}
  </span>
</template>

<script setup lang="ts">
defineProps<{
  icon: string;
  label: string;
}>();
</script>
