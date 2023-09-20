<template>
  <div
    role="button"
    :class="props.class"
    class="inline-flex items-center justify-center rounded-md text-sm font-medium transition-colors focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50 h-9 px-4 py-2"
  >
    <slot />
  </div>
</template>

<script setup>
const props = defineProps(['class']);
</script>

<style lang="scss" scoped></style>
