<template>
  <img :src="src" class="img-square-contain" />
</template>

<script setup lang="ts">
defineProps<{
  src: string;
}>();
</script>
