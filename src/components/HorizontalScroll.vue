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
import { inject, onMounted, ref } from 'vue';

interface Props {
  refKey: string;
  class?: string;
}

const props = withDefaults(defineProps<Props>(), {
  class: '',
});

const scrollRefs = ref<Record<string, HTMLElement | null>>({});
const applyScrollBehavior = inject<(el: HTMLElement) => void>('applyScrollBehavior')!;

onMounted(() => {
  const el = scrollRefs.value?.[props.refKey];

  if (!el) {
    console.error(`Element with refKey "${props.refKey}" not found.`);
    return;
  }
  if (el) {
    applyScrollBehavior(el);
  }
});
</script>
