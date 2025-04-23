<template>
  <q-layout view="lHh Lpr lFf" class="q-mx-auto" style="max-width: 420px">
    <app-header />
    <q-page-container>
      <q-page rounded-md>
        <banner-section />
        <feature-cards />

        <scrollable-section
          icon="star"
          icon-color="yellow"
          title="Trending"
          ref-key="trendingScroll"
          class="q-mt-md bg-white q-by-md"
        >
          <product-card v-for="(_, index) in 5" :key="index" />
        </scrollable-section>

        <div class="q-mt-md bg-gradient">
          <sale-timer-card />
          <div class="q-my-md q-pa-md">
            <horizontal-scroll ref-key="saleProductScroll">
              <product-card-mini v-for="(_, index) in 5" :key="index" />
            </horizontal-scroll>
          </div>
        </div>

        <scrollable-section
          icon="emoji_events"
          icon-color="amber"
          title="Best sellers"
          ref-key="bestsellerScroll"
          class="q-mt-md bg-white q-py-xs"
        >
          <product-card v-for="(_, index) in 5" :key="index" />
        </scrollable-section>

        <scrollable-section
          icon="emoji_events"
          icon-color="amber"
          title="New Arrivals"
          ref-key="scrollRow"
          class="q-mt-md no-shadow bg-white q-py-xs"
          bordered
        >
          <product-card v-for="(_, index) in 5" :key="index" />
        </scrollable-section>

        <q-card bordered class="no-shadow q-my-md bg-white" style="overflow: hidden">
          <horizontal-scroll ref-key="beginnerSlider" class="q-py-md q-px-md">
            <beginner-card v-for="i in 5" :key="i" />
          </horizontal-scroll>
        </q-card>

        <store-section />

        <categories-section :categories="categories" />

        <brands-section :brands="brands" />

        <scrollable-section
          title="Featured reviews"
          ref-key="featureCardsScroll"
          class="no-shadow bg-white q-mb-md"
          bordered
        >
          <item-feeback v-for="i in 5" :key="i" />
        </scrollable-section>

        <trust-badges-section />

        <product-tabs-section />
      </q-page>
    </q-page-container>

    <app-footer :items="navigationItems" />
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

.flex-center {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 0.2rem;
}

.bg-gradient {
  background-image: linear-gradient(to bottom, white, #ffffff, #ffd1d1);
}

.bg-gradient-percent {
  background-image: linear-gradient(to right, #f8c7c7bd, #fadddd);
  padding: 0.1rem 0.4rem;
  border-radius: 8px;
}

.bg-gradient-img {
  background-image: linear-gradient(to bottom, #f8c7c7bd, #fadddd);
  padding: 0.5rem 0.5rem;
  height: 100px;
}

.box-radius {
  border-radius: 0.6rem !important;
}

.border-top-x {
  border-top-left-radius: 0.2rem !important;
  border-top-right-radius: 0.2rem !important;
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

.scrollable-row {
  overflow-x: auto;
  scroll-behavior: smooth;
  user-select: none;
  -webkit-overflow-scrolling: touch;
  scrollbar-width: none;
  -ms-overflow-style: none;
  flex-direction: row;
  gap: 24px;
  flex-wrap: nowrap;
  cursor: grab;
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

.btn-view-product {
  color: var(--q-primary);
  background: white;
  border-radius: 1rem;
  border: 1px solid var(--q-primary);
  font-size: 10px;
  padding: 0.2rem 0.5rem;
}

.text-underline {
  text-decoration: underline;
  text-decoration-color: var(--q-primary);
  text-decoration-thickness: 4px;
  text-underline-offset: 2px;
}
.font-xs {
  font-size: 10px;
}

.font-sm {
  font-size: 14px;
}
.border-light {
  border: 1px solid #eee;
}
.img-square-contain {
  height: 30px;
  aspect-ratio: 1 / 1;
  object-fit: contain;
}
.clamp-3 {
  overflow: hidden;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
}
</style>

<script setup lang="ts">
import AppHeader from 'components/partials/Header.vue';
import BannerSection from 'components/BannerSection.vue';
import FeatureCards from 'components/FeatureCards.vue';
import ProductCard from 'src/components/ProductCard.vue';
import ProductCardMini from 'src/components/ProductCardMini.vue';
import ItemFeeback from 'src/components/ItemFeeback.vue';
import ScrollableSection from 'src/components/ScrollableSection.vue';
import HorizontalScroll from 'src/components/HorizontalScroll.vue';
import SaleTimerCard from 'src/components/SaleTimerCard.vue';
import BeginnerCard from 'src/components/BeginnerCard.vue';
import StoreSection from 'src/components/StoreSection.vue';
import CategoriesSection from 'src/components/CategoriesSection.vue';
import BrandsSection from 'src/components/BrandsSection.vue';
import TrustBadgesSection from 'src/components/TrustBadgesSection.vue';
import ProductTabsSection from 'src/components/ProductTabsSection.vue';
import AppFooter from 'src/components/partials/Footer.vue';
import type { Category, Brand, NavigationItem } from 'src/types';

const categories: Category[] = [
  { name: 'Nail Polish Essentials', image: 'https://placeholder.com/150x150' },
  { name: 'Sculpture/ Builder Gel', image: 'https://placeholder.com/150x150' },
  { name: '3D Charms/ Rhinestones', image: 'https://placeholder.com/150x150' },
  { name: 'Art Flakes/ Foils', image: 'https://placeholder.com/150x150' },
  { name: 'Chrome', image: 'https://placeholder.com/150x150' },
  { name: 'Nail Art Gel/ Lacquer', image: 'https://placeholder.com/150x150' },
];

const brands: Brand[] = [
  { name: 'IGEL', logo: 'https://placeholder.com/100x60' },
  { name: 'DND', logo: 'https://placeholder.com/100x60' },
  { name: 'IRIS', logo: 'https://placeholder.com/100x60' },
  { name: 'NGHIA NIPPERS', logo: 'https://placeholder.com/100x60' },
  { name: 'KUPA', logo: 'https://placeholder.com/100x60' },
  { name: 'APRÉS', logo: 'https://placeholder.com/100x60' },
];

const navigationItems: NavigationItem[] = [
  { name: 'Marketplace', icon: 'home' },
  { name: 'Categories', icon: 'grid_view' },
  { name: 'Cart', icon: 'shopping_cart' },
  { name: 'Posts', icon: 'work' },
  { name: 'Account', icon: 'person' },
];
</script>
