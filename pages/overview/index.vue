<template>
  <div className="flex flex-col gap-4 items-center">
    <photo-icon class="text-gray-500 h-16" />
    <h1 className="text-2xl">Get started by training your first model.</h1>
    <div>
      <NuxtLink to="/overview/models/train">
        <ButtonComponent
          class="bg-primary text-white hover:bg-primary/90 h-10 px-8"
          >Train model</ButtonComponent
        >
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
import { PhotoIcon } from '@heroicons/vue/24/solid';
</script>

<style lang="scss" scoped></style>
