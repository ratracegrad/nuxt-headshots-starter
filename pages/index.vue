<template>
  <div class="flex flex-col items-center pt-16">
    <div
      class="flex flex-col lg:flex-row items-center gap-8 p-8 max-w-6xl w-full"
    >
      <div class="flex flex-col space-y-4 lg:w-1/2 w-full">
        <h1 class="text-5xl font-bold">
          Professional AI Headshots in minutes.
        </h1>
        <p class="text-gray-600 text-lg">
          Elevate your online presence with HD headshots generated by our AI.
          Ideal for social profiles, resumes, and professional portfolios.
        </p>
        <div class="flex flex-col space-y-2">
          <NuxtLink to="/login">
            <ButtonComponent
              class="w-full lg:w-1/2 bg-primary text-white shadow hover:bg-primary/90"
            >
              Get Your Headshots
            </ButtonComponent>
          </NuxtLink>
          <p class="text-sm text-gray-500 italic">
            Trusted by professionals worldwide. Quick and efficient.
          </p>
        </div>
        <div class="mt-4 text-gray-500">
          <span>Already a member? </span>
          <NuxtLink class="text-primary hover:underline" to="/login">
            Sign In
          </NuxtLink>
        </div>
      </div>
      <div class="lg:w-1/2 w-full mt-8 lg:mt-0">
        <img
          src="~/assets/img/hero.png"
          alt="AI Headshot Illustration"
          class="rounded-lg object-cover w-full h-full"
        />
      </div>
    </div>
    <ExplainerSection />
    <PricingSection />
  </div>
</template>

<script setup>
useHead({
  title: 'Nuxt Headshots AI',
});
</script>

<style lang="scss" scoped></style>
