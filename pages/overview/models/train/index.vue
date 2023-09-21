<template>
  <div className="w-full max-w-2xl mx-auto">
    <div id="train-model-container" className="flex flex-1 flex-col gap-2 px-2">
      <NuxtLink to="/overview" className="text-sm">
        <ButtonComponent
          class="border border-input bg-transparent shadow-sm hover:bg-accent hover:text-accent-foreground mb-2"
        >
          <!-- <ArrowLeftIcon className="mr-2" /> -->
          <div>← Go Back</div>
        </ButtonComponent>
      </NuxtLink>

      <!-- card -->
      <div class="rounded-xl border bg-card text-card-foreground shadow">
        <!-- card header -->
        <div class="flex flex-col space-y-1.5 p-6">
          <!-- card title -->
          <p class="font-semibold leading-none tracking-tight">Train Model</p>
          <!-- card description -->
          <p class="text-sm text-muted-foreground">
            Choose a name, type, and upload some photos to get started.
          </p>
        </div>

        <!-- card content -->
        <div class="p-6 pt-0">
          <TrainModelZone />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ArrowLeftIcon } from '@heroicons/vue/24/solid';
</script>

<style lang="scss" scoped></style>
