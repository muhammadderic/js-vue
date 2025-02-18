<script setup>
// import { defineAsyncComponent } from 'vue';
import LoadingSpinner from '@/components/LoadingSpinner.vue';
import CarouselCompt from '@/components/CarouselCompt.vue';
import NavBar from '@/components/NavBar.vue';

// const CarouselCompt = defineAsyncComponent({
//   loader: () => import('@/components/CarouselCompt.vue'),
//   delay: 5000, // Show spinner only after 3 seconds
// });
</script>

<template>
  <Suspense>
    <template #default>
      <div>
      <NavBar/>
      <CarouselCompt/>
      </div>
    </template>

    <template #fallback>
      <LoadingSpinner />
    </template>
  </Suspense>
</template>