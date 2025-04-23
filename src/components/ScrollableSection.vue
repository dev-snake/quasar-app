<template>
  <q-card :class="props.class" :bordered="props.bordered" flat>
    <div class="row items-center q-mb-sm q-px-xs">
      <q-icon
        v-if="props.icon"
        :name="props.icon"
        :color="props.iconColor"
        size="sm"
        class="q-mr-sm"
      />
      <div class="text-subtitle2 text-grey-7">{{ props.title }}</div>
      <q-space />
      <q-icon name="arrow_forward" size="xs" />
    </div>

    <horizontal-scroll :ref-key="props.refKey" class="q-pl-md">
      <slot></slot>
    </horizontal-scroll>
  </q-card>
</template>

<script setup lang="ts">
import HorizontalScroll from './HorizontalScroll.vue';

interface Props {
  title: string;
  icon?: string | null;
  iconColor?: string;
  refKey: string;
  class?: string;
  bordered?: boolean;
}

const props = withDefaults(defineProps<Props>(), {
  icon: null,
  iconColor: 'grey',
  class: '',
  bordered: false,
});
</script>
