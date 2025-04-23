<template>
  <q-footer class="bg-white q-mx-auto q-mt-lg q-mb-md" style="max-width: 420px">
    <div class="row justify-between q-px-md">
      <div
        class="text-center q-px-md q-py-xs"
        :class="{ 'text-primary': index === 0, 'text-black': index !== 0 }"
        v-for="(item, index) in items"
        :key="index"
      >
        <q-icon
          :name="item.icon"
          class="q-mx-xs"
          size="sm"
          :class="{ 'text-primary': index === 0, 'text-grey-9': index !== 0 }"
          style="color: var(--q-primary)"
        />
        <span class="block" style="font-size: 10px" v-text="item.name"></span>
      </div>
    </div>
  </q-footer>
</template>

<script setup lang="ts">
interface NavigationItem {
  name: string;
  icon: string;
}

defineProps<{
  items: NavigationItem[];
}>();
</script>
