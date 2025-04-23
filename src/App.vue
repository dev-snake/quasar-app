<template>
  <router-view />
</template>

<script setup lang="ts">
import { ref, provide } from 'vue';

const scrollRefs = ref<Record<string, HTMLElement>>({});
provide('scrollRefs', scrollRefs);

const applyScrollBehavior = (el: HTMLElement): void => {
  let isDown = false;
  let startX = 0;
  let scrollLeft = 0;

  const onMouseDown = (e: MouseEvent): void => {
    isDown = true;
    el.classList.add('active');
    startX = e.pageX - el.offsetLeft;
    scrollLeft = el.scrollLeft;
  };

  const onMouseLeave = (): void => {
    isDown = false;
    el.classList.remove('active');
  };

  const onMouseUp = (): void => {
    isDown = false;
    el.classList.remove('active');
  };

  const onMouseMove = (e: MouseEvent): void => {
    if (!isDown) return;
    e.preventDefault();
    const x = e.pageX - el.offsetLeft;
    const walk = (x - startX) * 1.5;
    el.scrollLeft = scrollLeft - walk;
  };

  const onTouchStart = (e: TouchEvent): void => {
    isDown = true;
    el.classList.add('active');
    startX = (e.touches[0] ? e.touches[0].pageX : 0) - el.offsetLeft;
    scrollLeft = el.scrollLeft;
  };

  const onTouchEnd = (): void => {
    isDown = false;
    el.classList.remove('active');
  };

  const onTouchMove = (e: TouchEvent): void => {
    if (!isDown) return;
    const x = (e.touches[0] ? e.touches[0].pageX : 0) - el.offsetLeft;
    const walk = (x - startX) * 1.5;
    el.scrollLeft = scrollLeft - walk;
  };

  el.addEventListener('mousedown', onMouseDown);
  el.addEventListener('mouseleave', onMouseLeave);
  el.addEventListener('mouseup', onMouseUp);
  el.addEventListener('mousemove', onMouseMove);

  el.addEventListener('touchstart', onTouchStart);
  el.addEventListener('touchend', onTouchEnd);
  el.addEventListener('touchmove', onTouchMove);
};

provide('applyScrollBehavior', applyScrollBehavior);
</script>
