<template>
  <q-layout view="lHh Lpr lFf" class="q-mx-auto" style="max-width: 420px">
    <q-header class="q-mx-auto bg-white no-shadow" style="max-width: 420px">
      <div class="row justify-between items-center q-pt-xs q-pb-xs q-pl-xs q-pr-xs">
        <q-icon tag="i" class="bx bx-heart text-black text-h5" />
        <q-typography tag="h1" class="text-black text-h6" style="font-weight: 600"
          >Marketplace</q-typography
        >
        <q-icon tag="i" class="bx bx-cart-alt text-black text-h5" />
      </div>
      <div class="relative-position">
        <input type="text" class="q-w-full q-ml-xs q-mr-xs w-full input-search" />
        <q-icon
          tag="i"
          class="bx bx-search text-black absolute"
          style="top: 50%; transform: translate(1rem, -50%)"
        />
      </div>
    </q-header>
    <q-page-container>
      <q-page rounded-md>
        <q-banner dense class="bg-gradient">
          <img
            src="https://nailzy.com/_next/image?url=https%3A%2F%2Fcdn.nailzy.com%2Fbanners%2F67f93a317148ddc3a9a9d127&w=1200&q=75"
            alt=""
            class="w-full rounded-borders"
          />
        </q-banner>
        <!--  -->
        <div class="no-shadow row justify-between bg-white q-pl-xs q-pr-xs q-pt-md q-pb-md">
          <q-card class="no-shadow col-6">
            <q-card-section class="text-primary q-py-none q-px-xs w-full">
              <div class="box-radius q-px-md" style="border: 1px solid">
                <h6 class="q-ma-none" style="font-size: 1rem !important">Sustainability</h6>
                <div class="flex-center">
                  <span style="font-size: 10px">At nailzy</span>
                  <q-icon name="eco" class="text-pink" />
                </div>
              </div>
            </q-card-section>
          </q-card>
          <q-card class="no-shadow col-6">
            <q-card-section class="text-primary q-py-none q-px-xs rounded-lg">
              <div class="box-radius q-px-md" style="border: 1px solid">
                <h6 class="q-pt-lg-xs q-ma-none" style="font-size: 1rem !important">
                  Free shipping
                </h6>
                <div class="flex-center">
                  <span style="font-size: 10px">On eligible orders</span>
                  <q-icon name="local_shipping" class="text-pink" />
                </div>
              </div>
            </q-card-section>
          </q-card>
        </div>
        <!--  -->
        <div class="q-pb-md">
          <div class="q-px-md">
            <div class="row items-center q-mb-md">
              <q-icon name="star" color="yellow" size="md" class="q-mr-sm" />
              <div class="text-h6">Trending</div>
              <q-space />
              <q-btn flat round dense icon="arrow_forward" />
            </div>

            <div class="row q-col-gutter-md">
              <div class="col-4">
                <q-card class="product-card">
                  <q-img src="https://placehold.co/150x150" />
                  <q-card-section class="q-pa-xs">
                    <div class="ellipsis-2-lines">FREE SHIPPING - N...</div>
                    <div class="row items-center">
                      <q-avatar size="20px" class="q-mr-xs">
                        <img src="https://placehold.co/20x20" />
                      </q-avatar>
                      <div class="text-caption">10 options</div>
                    </div>
                    <div class="text-caption">
                      From <span class="text-h6 text-red-8">$89.99</span>
                    </div>
                    <div class="row items-center">
                      <div class="text-caption q-mr-xs">0</div>
                      <q-icon name="star" color="amber" size="xs" />
                      <div class="text-caption q-ml-sm">Sold 1</div>
                    </div>
                  </q-card-section>
                </q-card>
              </div>
            </div>
          </div>
        </div>
        <!--  -->
        <div class="q-mt-md">
          <q-card class="bg-red text-white">
            <q-card-section class="row items-center no-wrap">
              <q-icon name="bolt" size="md" />
              <span>Egg-cellent Easter Sale!</span>
              <q-space />
              <div class="row">
                <div class="bg-white text-red q-px-sm q-py-xs rounded-borders">16</div>
                <div class="q-px-xs text-h6">:</div>
                <div class="bg-white text-red q-px-sm q-py-xs rounded-borders">28</div>
                <div class="q-px-xs text-h6">:</div>
                <div class="bg-white text-red q-px-sm q-py-xs rounded-borders">08</div>
                <q-btn icon="arrow_forward" flat round dense color="white" size="sm" />
              </div>
            </q-card-section>
          </q-card>
        </div>
        <!--  -->
        <div class="q-my-md bg-gradient">
          <div
            ref="scrollRow"
            class="row justify-between scrollable-row"
            style="flex-direction: row; gap: 4px; flex-wrap: nowrap; cursor: grab"
          >
            <div
              class="bg-white col-3 q-px-none shadow-1 rounded-borders"
              style="padding: 0 3px"
              v-for="i in [1, 2, 3, 4, 5]"
              :key="i"
            >
              <div class="rounded-borders w-full">
                <q-img src="/src/assets/images/img1.png" class="w-full border-top-x" />
                <div class="text-negative q-pb-none q-px-xs">
                  <span style="font-size: 12px">$</span
                  ><strong
                    style="display: inline-block; transform: translateY(4px); font-size: 16px"
                    >9</strong
                  ><span style="font-size: 12px">.90</span>
                </div>
                <div class="q-pt-none q-pb-xs q-px-xs row items-center justify-between">
                  <span style="font-size: 10px; color: gray; text-decoration: line-through"
                    >14.00</span
                  >
                  <span class="bg-gradient-percent text-negative" style="font-size: 10px">14%</span>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!--  -->
        <!-- Best Sellers Section -->
        <div class="q-mt-md bg-white q-py-xs" style="overflow: hidden">
          <div class="row items-center q-mb-sm q-px-xs">
            <q-icon name="emoji_events" color="amber" size="sm" class="q-mr-sm" />
            <div class="text-subtitle2 text-grey">Best sellers</div>
            <q-space />
            <q-icon name="chevron_right" />
          </div>

          <div
            ref="scrollRow"
            class="row justify-between q-col-gutter-sm scrollable-row q-pl-md"
            style="flex-direction: row; gap: 4px; flex-wrap: nowrap; cursor: grab"
          >
            <div class="col-4 q-px-xs q-py-xs" v-for="i in 10" :key="i">
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
                    <span class="text-grey text-caption q-pr-xs" style="font-size: 10px"
                      >From
                    </span>
                    <span class="text-subtitle2 text-red" style="font-size: 12px">$</span
                    ><strong
                      class="text-red"
                      style="display: inline-block; transform: translateY(2px); font-size: 16px"
                    >
                      9</strong
                    ><span class="text-red" style="font-size: 12px">.90</span>
                    <span
                      class="text-caption text-red text-grey q-ml-xs line-through"
                      style="font-size: 10px"
                      >$10.00</span
                    >
                  </div>
                  <div class="row items-center">
                    <div class="text-amber" style="font-size: 10px">5</div>
                    <q-icon name="star" color="amber" style="font-size: 14px" />
                    <div class="text-caption q-ml-sm text-grey" style="font-size: 10px">
                      Sold 3972
                    </div>
                  </div>
                </q-card-section>
              </q-card>
            </div>
          </div>
        </div>
        <!-- New Arrivals -->
        <div class="q-mt-md bg-white q-py-xs" style="overflow: hidden">
          <div class="row items-center q-mb-sm q-px-xs">
            <q-icon name="emoji_events" color="amber" size="sm" class="q-mr-sm" />
            <div class="text-subtitle2 text-grey">New Arrivals</div>
            <q-space />
            <q-icon name="chevron_right" />
          </div>

          <div
            ref="scrollRow"
            class="row justify-between q-col-gutter-sm scrollable-row q-px-xs q-pl-md"
            style="flex-direction: row; gap: 4px; flex-wrap: nowrap; cursor: grab"
          >
            <div class="col-4 q-px-xs q-py-xs" v-for="i in 10" :key="i">
              <q-card class="bg-white q-px-none shadow-1 rounded-borders">
                <q-img src="/src/assets/images/gt.png" />
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
                    <div style="font-size: 10px">3 options</div>
                  </div>

                  <div class="row no-wrap items-center">
                    <span class="text-grey text-caption q-pr-xs" style="font-size: 10px"
                      >From
                    </span>
                    <span class="text-subtitle2 text-red" style="font-size: 12px">$</span
                    ><strong
                      class="text-red"
                      style="display: inline-block; transform: translateY(2px); font-size: 16px"
                    >
                      9</strong
                    ><span class="text-red" style="font-size: 12px">.90</span>
                    <span
                      class="text-caption text-red text-grey q-ml-xs line-through"
                      style="font-size: 10px"
                      >$10.00</span
                    >
                  </div>
                  <div class="row items-center">
                    <div class="text-amber" style="font-size: 10px">5</div>
                    <q-icon name="star" color="amber" style="font-size: 14px" />
                  </div>
                </q-card-section>
              </q-card>
            </div>
          </div>
        </div>
        <!-- for slider -->
        <div class="q-my-md bg-white" style="overflow: hidden">
          <div
            ref="beginnerSlider"
            class="row no-wrap q-py-md q-px-md scrollable-row"
            style="flex-direction: row; gap: 8px; flex-wrap: nowrap; cursor: grab"
          >
            <q-card class="col-7 no-shadow shadow-custom" v-for="i in 5" :key="i">
              <div class="radius-top-x">
                <div class="border-top-x bg-gradient-img" />
              </div>
              <div class="row items-center justify-between q-mt-xs">
                <span class="q-px-xs">For Beginners</span>
                <q-icon name="chevron_right" size="sm" class="text-grey" />
              </div>
            </q-card>
          </div>
        </div>
        <!-- ATM  -->
        <div class="q-my-md">
          <q-card flat bordered class="q-pa-md">
            <div class="row">
              <div class="col-1">
                <q-icon name="check_circle" color="green" size="sm" />
              </div>
              <div class="col-10">
                <div class="text-weight-medium">Safe payments</div>
                <div class="q-mb-xs text-grey-7 q-mt-xs" style="font-size: 10px">
                  Shop confidently with our secure payment options. All card details are encrypted
                  for maximum protection during transactions.
                </div>
              </div>
            </div>

            <div class="q-pl-lg row q-mb-lg q-gutter-lg">
              <img
                src="https://raw.githubusercontent.com/datatrans/payment-logos/master/assets/cards/visa.svg"
                style="height: 30px; aspect-ratio: 1 / 1; object-fit: contain"
              />
              <img
                src="https://raw.githubusercontent.com/datatrans/payment-logos/master/assets/cards/mastercard.svg"
                style="height: 30px; aspect-ratio: 1 / 1; object-fit: contain"
              />
              <img
                src="https://raw.githubusercontent.com/datatrans/payment-logos/master/assets/cards/discover.svg"
                style="height: 30px; aspect-ratio: 1 / 1; object-fit: contain"
              />
              <img
                src="https://raw.githubusercontent.com/datatrans/payment-logos/master/assets/wallets/apple-pay.svg"
                style="height: 30px; aspect-ratio: 1 / 1; object-fit: contain"
              />
              <img
                src="https://raw.githubusercontent.com/datatrans/payment-logos/master/assets/wallets/google-pay.svg"
                style="height: 30px; aspect-ratio: 1 / 1; object-fit: contain"
              />
            </div>
            <div class="text-grey-7 w-full q-mb-md" style="border: 1px solid #eee" />

            <!--  -->
            <div class="row q-mb-lg">
              <div class="col-1">
                <q-icon name="check_circle" color="green" size="sm" />
              </div>
              <div class="col-10">
                <div class="text-weight-medium">Secure policy</div>
                <div class="q-mb-xs text-grey-7 q-mt-xs" style="font-size: 10px">
                  Your privacy matters to us. We guarantee that your personal information will never
                  be shared with third parties.
                </div>
              </div>
            </div>
            <!--  -->
            <div class="row">
              <div class="col-1">
                <q-icon name="phone" color="green" size="sm" class="q-mr-sm" />
              </div>
              <div class="col-10">
                <div class="text-weight-medium">Dedicated support</div>
                <div class="q-mb-xs text-grey-7 q-mt-xs" style="font-size: 10px">
                  Need help? Our dedicated support team is available by phone to assist with any
                  questions or issues you may have.
                </div>
              </div>
            </div>
          </q-card>
        </div>
      </q-page>
    </q-page-container>
  </q-layout>
</template>
<style>
* {
  font-family: 'Inter', sans-serif;
}
body {
  line-height: unset;
  background: #eee;
}
.w-full {
  width: 100%;
}
.h-full {
  height: 100%;
}
.input-search {
  background: #eee;
  border: none;
  outline: none;
  padding: 6px 2rem 0.5rem;
  border-radius: 2rem;
}
.bg-gradient {
  background-image: linear-gradient(to bottom, white, #ffffff, #ffd1d1);
  padding: 0.5rem 0.5rem;
}
.box-radius {
  border-radius: 0.6rem !important;
}
.flex-center {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 0.2rem;
}
.border-top-x {
  border-top-left-radius: 0.2rem !important;
  border-top-right-radius: 0.2rem !important;
}
.bg-gradient-percent {
  background-image: linear-gradient(to right, #f8c7c7bd, #fadddd);
  padding: 0.1rem 0.4rem;
  border-radius: 8px;
}

.scrollable-row {
  overflow-x: auto;
  scroll-behavior: smooth;
  user-select: none;
  -webkit-overflow-scrolling: touch;
  scrollbar-width: none;
  -ms-overflow-style: none;
}
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
.shadow-custom {
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
  border-radius: 0.6rem 0.6rem 0 0;
  border: 1px solid #eee;
}
.bg-gradient-img {
  background-image: linear-gradient(to bottom, #f8c7c7bd, #fadddd);
  padding: 0.5rem 0.5rem;
  height: 100px;
}
</style>
<script setup lang="ts">
import { ref, onMounted } from 'vue';

// Create refs for each scrollable section
const scrollRow = ref<HTMLDivElement | null>(null);
const beginnerSlider = ref<HTMLDivElement | null>(null);
// Create refs for your other sections too

// Add a function to apply scroll behavior to an element
const applyScrollBehavior = (el: HTMLDivElement) => {
  let isDown = false;
  let startX = 0;
  let scrollLeft = 0;

  const onMouseDown = (e: MouseEvent) => {
    isDown = true;
    el.classList.add('active');
    startX = e.pageX - el.offsetLeft;
    scrollLeft = el.scrollLeft;
  };

  const onMouseLeave = () => {
    isDown = false;
    el.classList.remove('active');
  };

  const onMouseUp = () => {
    isDown = false;
    el.classList.remove('active');
  };

  const onMouseMove = (e: MouseEvent) => {
    if (!isDown) return;
    e.preventDefault();
    const x = e.pageX - el.offsetLeft;
    const walk = (x - startX) * 1.5;
    el.scrollLeft = scrollLeft - walk;
  };

  el.addEventListener('mousedown', onMouseDown);
  el.addEventListener('mouseleave', onMouseLeave);
  el.addEventListener('mouseup', onMouseUp);
  el.addEventListener('mousemove', onMouseMove);
};

onMounted(() => {
  // Apply the behavior to each scrollable element
  if (scrollRow.value) applyScrollBehavior(scrollRow.value);
  if (beginnerSlider.value) applyScrollBehavior(beginnerSlider.value);
  // Apply to your other sections too
});
</script>
