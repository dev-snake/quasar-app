<template>
  <div
    :ref="
      (el) => {
        if (el) scrollRefs[props.refKey] = el as HTMLElement;
      }
    "
    class="row justify-between scrollable-row"
    :class="props.class"
  >
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
import { inject, onMounted } from 'vue';

interface Props {
  refKey: string;
  class?: string;
}

const props = withDefaults(defineProps<Props>(), {
  class: '',
});

const scrollRefs = inject<Record<string, HTMLElement>>('scrollRefs')!;
const applyScrollBehavior = inject<(el: HTMLElement) => void>('applyScrollBehavior')!;

onMounted(() => {
  const el = scrollRefs[props.refKey];
  if (el) {
    applyScrollBehavior(el);
  }
});
</script>
