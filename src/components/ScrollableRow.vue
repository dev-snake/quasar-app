<template>
  <div
    ref="scrollContainer"
    class="scrollable-row"
    :class="{ 'q-pl-md': paddingLeft, 'q-pr-md': paddingRight, 'q-px-md': paddingX }"
    :style="containerStyles"
  >
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount, computed } from 'vue';

const props = defineProps({
  paddingLeft: { type: Boolean, default: false },
  paddingRight: { type: Boolean, default: false },
  paddingX: { type: Boolean, default: false },
  gap: { type: Number, default: 8 },
});

const scrollContainer = ref<HTMLElement | null>(null);

const containerStyles = computed(() => ({
  'flex-direction': 'row',
  'flex-wrap': 'nowrap',
  cursor: 'grab',
  gap: `${props.gap}px`,
}));

// Hàm thiết lập scroll behavior với hỗ trợ cả chuột và touch
const setupScroll = () => {
  const el = scrollContainer.value;
  if (!el) return;

  let isDown = false;
  let startX = 0;
  let scrollLeft = 0;

  const onStart = (clientX: number) => {
    isDown = true;
    el.classList.add('active');
    startX = clientX - el.offsetLeft;
    scrollLeft = el.scrollLeft;
  };

  const onEnd = () => {
    isDown = false;
    el.classList.remove('active');
  };

  const onMove = (clientX: number) => {
    if (!isDown) return;
    const x = clientX - el.offsetLeft;
    const walk = (x - startX) * 1.5; // Tốc độ scroll
    el.scrollLeft = scrollLeft - walk;
  };

  // Sự kiện chuột
  const handleMouseDown = (e: MouseEvent) => onStart(e.pageX);
  const handleMouseLeave = onEnd;
  const handleMouseUp = onEnd;
  const handleMouseMove = (e: MouseEvent) => {
    if (!isDown) return;
    e.preventDefault();
    onMove(e.pageX);
  };

  // Sự kiện touch (cho thiết bị di động)
  const handleTouchStart = (e: TouchEvent) => onStart(e.touches[0].clientX);
  const handleTouchEnd = onEnd;
  const handleTouchMove = (e: TouchEvent) => {
    if (!isDown) return;
    onMove(e.touches[0].clientX);
  };

  // Thêm các event listeners
  el.addEventListener('mousedown', handleMouseDown);
  el.addEventListener('mouseleave', handleMouseLeave);
  el.addEventListener('mouseup', handleMouseUp);
  el.addEventListener('mousemove', handleMouseMove);

  el.addEventListener('touchstart', handleTouchStart);
  el.addEventListener('touchend', handleTouchEnd);
  el.addEventListener('touchmove', handleTouchMove);

  // Hàm dọn dẹp
  return () => {
    el.removeEventListener('mousedown', handleMouseDown);
    el.removeEventListener('mouseleave', handleMouseLeave);
    el.removeEventListener('mouseup', handleMouseUp);
    el.removeEventListener('mousemove', handleMouseMove);

    el.removeEventListener('touchstart', handleTouchStart);
    el.removeEventListener('touchend', handleTouchEnd);
    el.removeEventListener('touchmove', handleTouchMove);
  };
};

let cleanup: (() => void) | undefined;

onMounted(() => {
  cleanup = setupScroll();
});

onBeforeUnmount(() => {
  if (cleanup) cleanup();
});
</script>

<style scoped>
.scrollable-row {
  display: flex;
  overflow-x: auto;
  scroll-behavior: smooth;
  user-select: none;
  -webkit-overflow-scrolling: touch;
  scrollbar-width: none; /* Firefox */
  -ms-overflow-style: none; /* IE and Edge */
  position: relative;
}

.scrollable-row::-webkit-scrollbar {
  display: none; /* Chrome, Safari, Opera */
}

.scrollable-row.active {
  cursor: grabbing;
}

/* Hiệu ứng mượt mà khi scroll */
@media (prefers-reduced-motion: no-preference) {
  .scrollable-row {
    scroll-behavior: smooth;
  }
}

/* Hiệu ứng chỉ báo có thể scroll */
.scrollable-row::after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 24px;
  background: linear-gradient(to right, transparent, rgba(255, 255, 255, 0.8));
  pointer-events: none;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.scrollable-row:not(.no-overflow)::after {
  opacity: 1;
}
</style>
