<template>
  <div class="q-pb-md">
    <q-card
      class="no-shadow bg-white col-6 q-px-none q-px-xs q-py-xs"
      bordered
      style="border: 1px solid #eee"
    >
      <div class="row justify-between no-wrap">
        <span class="ellipsis q-mr-md" style="font-size: 10px">Tam H. </span>
        <div class="row items-center no-wrap q-mr-lg">
          <q-icon
            name="star"
            color="amber"
            size="xs"
            style="font-size: 10px"
            v-for="i in 5"
            :key="i"
          />
        </div>
      </div>
      <span class="text-caption text-warning">Very satisfied </span>
      <p
        class="q-mb-lg text-caption clamp-3"

      >
        App rất dễ sử dụng. Nhân viên rất nhiệt tình. Sản phẩm rất tốt.
      </p>
      <div class="q-mt-lg" style="border: solid 1px #eee"></div>
      <p class="q-mt-xs q-pa-none" style="font-size: 11px; display: inline">
        Paraffin Liner (LD) Thick - 30mic- 4 pcs
      </p>
      <span style="font-size: 9px">30mic- 4 pcs (650 bags)</span>
      <div class="row items-end q-mt-xs">
        <div class="text-negative q-pb-none q-px-xs">
          <span style="font-size: 12px">$</span
          ><strong style="display: inline-block; transform: translateY(4px); font-size: 16px"
            >9</strong
          ><span style="font-size: 12px">.90</span>
        </div>
        <div class="q-px-xs row items-center justify-between">
          <span style="font-size: 10px; color: gray">$25.00</span>
        </div>
      </div>
      <button class="q-mt-sm w-full btn-view-product">View Product</button>
    </q-card>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped></style>
