<template>
  <div class="col-4 q-px-xs q-py-xs">
    <q-card class="bg-white w-full q-px-none shadow-1 rounded-borders">
      <q-img src="/src/assets/images/bestseller.png" />
      <q-card-section class="q-pa-xs">
        <div class="ellipsis text-caption">Nitro Dipping Powder - Ombre Collection</div>
        <div class="row items-center q-mt-xs q-col-gutter-sm">
          <div class="avatar-stack row no-wrap">
            <q-avatar size="20px" class="avatar-item">
              <img src="https://placehold.co/20x20" />
            </q-avatar>
            <q-avatar size="20px" class="avatar-item">
              <img src="https://placehold.co/20x20" />
            </q-avatar>
            <q-avatar size="20px" class="avatar-item">
              <img src="https://placehold.co/20x20" />
            </q-avatar>
          </div>
          <div style="font-size: 10px">10 options</div>
        </div>

        <div class="row no-wrap items-center">
          <span class="text-grey text-caption q-pr-xs" style="font-size: 10px">From </span>
          <span class="text-subtitle2 text-red" style="font-size: 12px">$</span
          ><strong
            class="text-red"
            style="display: inline-block; transform: translateY(2px); font-size: 16px"
          >
            9</strong
          ><span class="text-red" style="font-size: 12px">.90</span>
          <span class="text-caption text-red text-grey q-ml-xs line-through" style="font-size: 10px"
            >$10.00</span
          >
        </div>
        <div class="row items-center">
          <div class="text-amber font-xs">5</div>
          <q-icon name="star" color="amber" class="font-sm" />
          <div class="text-caption q-ml-sm text-grey font-xs" >Sold 3972</div>
        </div>
      </q-card-section>
    </q-card>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.scrollable-row.active {
  cursor: grabbing;
}
.avatar-stack {
  display: flex;
  align-items: center;
}

.avatar-item {
  border: 1px solid white;
  margin-left: -8px;
}

.avatar-item:first-child {
  margin-left: 0;
}
</style>
