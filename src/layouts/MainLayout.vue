<template>
  <q-layout view="lHh Lpr lFf" class="q-mx-auto" style="max-width: 420px">
    <!-- <q-header class="q-mx-auto bg-white no-shadow" style="max-width: 420px">
      <div class="row justify-between items-center q-pt-xs q-pb-xs q-pl-xs q-pr-xs">
        <q-icon tag="i" class="bx bx-heart text-black text-h5" />
        <q-typography tag="h1" class="text-black text-h6" style="font-weight: 600"
          >Marketplace</q-typography
        >
        <q-icon tag="i" class="bx bx-cart-alt text-black text-h5" />
      </div>
      <div class="relative-position q-px-xs">
        <input type="text" class="w-full input-search" />
        <q-icon
          tag="i"
          class="bx bx-search text-black absolute"
          style="top: 50%; transform: translate(1rem, -50%); left: 0"
        />
      </div>
    </q-header> -->
    <app-header />
    <q-page-container>
      <q-page rounded-md>
        <!-- <q-banner dense class="bg-gradient">
          <img
            src="https://nailzy.com/_next/image?url=https%3A%2F%2Fcdn.nailzy.com%2Fbanners%2F67f93a317148ddc3a9a9d127&w=1200&q=75"
            alt=""
            class="w-full rounded-borders"
          />
        </q-banner> -->
        <banner-section />
        <!--  -->
        <feature-cards />
        <!-- <div class="no-shadow row justify-between bg-white q-pl-xs q-pr-xs q-pt-md q-pb-md">
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
        </div> -->
        <!--  -->
        <div class="q-mt-md bg-white q-py-md" style="overflow: hidden">
          <div class="row items-center q-mb-sm q-px-xs">
            <q-icon name="star" color="yellow" size="md" class="q-mr-sm text-caption" />
            <div class="text-subtitle2 text-grey-7">Trendding</div>
            <q-space />
            <q-icon name="arrow_forward" size="xs" />
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
        <!--  -->
        <div class="q-mt-md bg-gradient">
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
          <div class="q-my-md q-pa-md">
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
                    <span class="bg-gradient-percent text-negative" style="font-size: 10px"
                      >14%</span
                    >
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!--  -->
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
        <q-card class="q-mt-md no-shadow bg-white q-py-xs" bordered style="overflow: hidden">
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
        </q-card>
        <!-- for slider -->
        <q-card bordered class="no-shadow q-my-md bg-white" style="overflow: hidden">
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
        </q-card>
        <!-- ATM  -->
        <q-card class="q-my-md no-shadow bg-white" bordered>
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
        </q-card>
        <!--  -->
        <q-card class="q-my-md bg-white" bordered flat>
          <q-card class="bg-white no-shadow row justify-between items-center q-pa-md">
            <div class="row items-center">
              <q-icon class="bx bx-store q-mr-xs text-grey" size="xs" tag="i"></q-icon>
              <q-badge
                class="shipping-badge q-py-xs q-px-sm"
                color="pink-1"
                text-color="primary"
                align="middle"
                style="border-radius: 16px"
              >
                <q-icon name="local_shipping" class="q-mr-xs text-caption" />
                Ships from Nailzy
              </q-badge>
            </div>
            <div>
              <q-icon name="arrow_forward" size="xs" class="" />
            </div>
          </q-card>
          <div class="bg-white rounded-borders">
            <div class="q-px-md" style="overflow-x: auto">
              <div
                ref="storeRowScroll"
                class="row no-wrap q-gutter-x-md q-pb-md scrollable-row"
                style="flex-direction: row; gap: 8px; flex-wrap: nowrap; cursor: grab"
              >
                <q-card class="col-5" flat v-for="i in 5" :key="i">
                  <q-item class="q-py-xs row q-gutter-xs bg-secondary shadow-custom-v2 q-mt-xs">
                    <q-img
                      src="/src/assets/images/store.png"
                      class="rounded-borders"
                      style="width: 60px; height: 60px"
                    />
                    <q-item-section class="q-pa-none">
                      <div class="row items-center">
                        <q-icon
                          class="bx bx-store q-mr-xs text-grey text-caption"
                          size="xs"
                          tag="i"
                        ></q-icon>
                        <span class="ellipsis text-caption">EV Store</span>
                      </div>
                      <span class="text-grey q-mt-xs" style="font-size: 10px">Garland, TX</span>
                      <div class="row items-center q-mt-xs">
                        <div class="row items-center">
                          <q-icon name="star" color="amber" style="font-size: 14px" />
                          <span class="text-grey" style="font-size: 10px">(2)</span>
                        </div>
                      </div>
                    </q-item-section>
                  </q-item>
                </q-card>
              </div>
            </div>
          </div>
        </q-card>
        <!--  -->
        <q-card class="no-shadow q-mb-md" bordered>
          <div class=" ">
            <div class="row items-center q-mb-sm q-px-md q-pt-md">
              <div class="text-subtitle2">Featured categories</div>
              <q-space />
              <q-icon name="arrow_forward" size="xs" class="" />
            </div>

            <div
              class="category-scroll row no-wrap q-gutter-md q-pb-md q-px-md"
              style="overflow: hidden"
            >
              <div
                v-for="(category, index) in categories"
                :key="index"
                class="text-center col-2"
                style="max-width: 60px"
              >
                <q-img
                  src="/src/assets/images/logo2.png"
                  spinner-color="primary"
                  fit="cover"
                  style="border-radius: 50%; height: 60px; width: 60px; border: 1px solid #eee"
                />
                <span class="q-mt-sm" style="font-size: 10px; width: 60px">
                  {{ category.name }}
                </span>
              </div>
            </div>
          </div>
        </q-card>
        <!-- hot brand -->
        <q-card class="no-shadow bg-white q-mb-md" bordered>
          <div class="row items-center q-mb-sm q-px-md q-pt-md">
            <div class="text-subtitle2">Hot brands</div>
            <q-space />
            <q-icon name="arrow_forward" size="xs" class="" />
          </div>
          <div class="brands-scroll q-px-md row no-wrap overflow-hidden q-gutter-md">
            <div v-for="(brand, index) in brands" :key="index" class="text-center q-pb-md">
              <q-card class="no-shadow bg-white q-px-none" style="border: 1px solid #eee">
                <q-img
                  src="/src/assets/images/hot_branch.png"
                  spinner-color="primary"
                  height="60px"
                  fit="cover"
                  style="height: 60px; width: 60px"
                />
              </q-card>
              <span class="" style="font-size: 10px; width: 60px">
                {{ brand.name }}
              </span>
            </div>
          </div>
        </q-card>
        <!-- reviews -->
        <q-card class="no-shadow bg-white q-mb-md" bordered>
          <div class="row items-center q-mb-sm q-px-md q-pt-md">
            <div class="text-subtitle2">Featured reviews</div>
            <q-space />
          </div>
          <div class="brands-scroll q-px-md row no-wrap overflow-hidden q-gutter-md">
            <div v-for="(brand, index) in brands" :key="index" class="q-pb-md">
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
                  class="q-mb-lg text-caption"
                  style="
                    overflow: hidden;
                    display: -webkit-box;
                    -webkit-box-orient: vertical;
                    -webkit-line-clamp: 3;
                  "
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
                    ><strong
                      style="display: inline-block; transform: translateY(4px); font-size: 16px"
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
          </div>
        </q-card>
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
  /* padding: 0.5rem 0.5rem; */
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
  border: 2px solid #eee;
}
.shadow-custom-v2 {
  border-radius: 0.4rem !important;
  padding: 0.2rem !important;
  border: 1px solid rgb(231, 230, 230) !important;
}
.bg-gradient-img {
  background-image: linear-gradient(to bottom, #f8c7c7bd, #fadddd);
  padding: 0.5rem 0.5rem;
  height: 100px;
}
.btn-view-product {
  color: var(--q-primary);
  background: white;
  border-radius: 1rem;
  border: 1px solid var(--q-primary);
  font-size: 10px;
  padding: 0.2rem 0.5rem;
}
</style>
<script setup lang="ts">
import { ref, onMounted } from 'vue';
import AppHeader from 'components/partials/Header.vue';
import BannerSection from 'components/BannerSection.vue';
import FeatureCards from 'components/FeatureCards.vue';
// Create refs for each scrollable section
const scrollRow = ref<HTMLDivElement | null>(null);
const beginnerSlider = ref<HTMLDivElement | null>(null);
const storeRowScroll = ref<HTMLDivElement | null>(null);
// Create refs for your other sections too
const categories = [
  {
    name: 'Nail Polish Essentials',
    image: 'https://placeholder.com/150x150',
  },
  {
    name: 'Sculpture/ Builder Gel',
    image: 'https://placeholder.com/150x150',
  },
  {
    name: '3D Charms/ Rhinestones',
    image: 'https://placeholder.com/150x150',
  },
  {
    name: 'Art Flakes/ Foils',
    image: 'https://placeholder.com/150x150',
  },
  {
    name: 'Chrome',
    image: 'https://placeholder.com/150x150',
  },
  {
    name: 'Nail Art Gel/ Lacquer',
    image: 'https://placeholder.com/150x150',
  },
];
const brands = [
  {
    name: 'IGEL',
    logo: 'https://placeholder.com/100x60',
  },
  {
    name: 'DND',
    logo: 'https://placeholder.com/100x60',
  },
  {
    name: 'IRIS',
    logo: 'https://placeholder.com/100x60',
  },
  {
    name: 'NGHIA NIPPERS',
    logo: 'https://placeholder.com/100x60',
  },
  {
    name: 'KUPA',
    logo: 'https://placeholder.com/100x60',
  },
  {
    name: 'APRÉS',
    logo: 'https://placeholder.com/100x60',
  },
];
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
  if (storeRowScroll.value) applyScrollBehavior(storeRowScroll.value);
  // Apply to your other sections too
});
</script>
