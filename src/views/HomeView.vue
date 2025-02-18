<script setup lang="ts">
import { defineAsyncComponent } from 'vue';
import LoadingSpinner from '@/components/LoadingSpinner.vue';

const CarouselCompt = defineAsyncComponent({
  loader: () => import('@/components/CarouselCompt.vue'),
  delay: 5000, // Show spinner only after 3 seconds
});
</script>

<template>
  <Suspense>
    <template #default>
      <CarouselCompt/>
    </template>

    <template #fallback>
      <LoadingSpinner />
    </template>
  </Suspense>
</template>