<template>
  <div class="w-full max-w-6xl mt-16 mb-16 p-8 rounded-lg space-y-8">
    <h2 class="text-3xl font-bold text-center mb-8">Pricing</h2>
    <div
      class="flex flex-wrap justify-center lg:space-x-4 space-y-4 lg:space-y-0 items-stretch"
    >
      <div
        v-for="(option, index) in pricingOptions"
        :key="index"
        :class="`flex flex-col border rounded-lg p-4 w-full lg:w-1/4 ${option.bgColor}`"
      >
        <div class="flex-grow space-y-4">
          <h3 class="text-2xl font-semibold text-center">
            {{ option.title }}
          </h3>
          <p class="text-xl font-bold text-center mb-2">
            {{ option.price }}
          </p>
          <p class="text-sm text-gray-600 text-center">
            {{ option.description }}
          </p>
          <ul class="space-y-2 mb-4 pl-4">
            <li
              v-for="(feature, fIndex) in option.features"
              :key="fIndex"
              class="flex items-center space-x-2"
            >
              <span class="text-green-500">✔</span>
              <span>{{ feature }}</span>
            </li>
          </ul>
        </div>
        <div class="mt-10 text-center">
          <NuxtLink to="/login">
            <ButtonComponent
              class="w-3/4 bg-primary text-white shadow hover:bg-primary/90"
            >
              {{ option.buttonText }}
            </ButtonComponent>
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const pricingOptions = [
  {
    title: 'Starter',
    price: '$9.99/month',
    description:
      'Perfect for individuals looking to enhance their online presence.',
    features: [
      '5 AI Headshots',
      'Standard Resolution Downloads',
      'Personal Use License',
    ],
    buttonText: 'Choose Starter',
    bgColor: 'bg-white',
  },
  {
    title: 'Basic',
    price: '$19.99/month',
    description:
      'Ideal for professionals requiring frequent updates to their profiles.',
    features: [
      '15 AI Headshots',
      'High-Resolution Downloads',
      'Commercial Use License',
    ],
    buttonText: 'Choose Basic',
    bgColor: 'bg-blue-50',
  },
  {
    title: 'Premium',
    price: '$29.99/month',
    description: 'The best value with unlimited possibilities.',
    features: [
      '150 AI Headshots',
      'Ultra High-Resolution Downloads',
      'Extended Commercial Use License',
    ],
    buttonText: 'Choose Premium',
    bgColor: 'bg-white',
  },
];
</script>

<style lang="scss" scoped></style>
