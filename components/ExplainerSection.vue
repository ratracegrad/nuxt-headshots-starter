<template>
  <div class="w-full max-w-6xl mt-16 p-8 bg-gray-100 rounded-lg space-y-8">
    <h2 class="text-3xl font-bold text-center mb-8">How It Works</h2>

    <!--  Step 1: Upload your images  -->
    <div class="space-y-4">
      <div class="flex items-center justify-center space-x-4">
        <div
          class="text-3xl font-bold text-blue-600 bg-white border-2 border-blue-600 rounded-full w-10 h-10 flex items-center justify-center"
        >
          1
        </div>
        <h3 class="text-2xl font-semibold">Upload your images</h3>
      </div>
      <p class="text-sm text-gray-600 text-center">
        Upload 4+ high-quality selfies: front facing, 1 person in frame, no
        glasses or hats.
      </p>
      <img
        src="~/assets/img/example.png"
        alt="AI Headshot example"
        class="rounded-lg object-cover w-full md:w-3/4 lg:w-1/2 mx-auto"
      />
    </div>

     <!-- Step 2: Train your model  -->
    <div class="space-y-4">
      <div class="flex items-center justify-center space-x-4">
        <div
          class="text-3xl font-bold text-blue-600 bg-white border-2 border-blue-600 rounded-full w-10 h-10 flex items-center justify-center"
        >
          2
        </div>
        <h3 class="text-2xl font-semibold">Our AI gets to work</h3>
      </div>
      <p class="text-sm text-gray-600 text-center">
        The AI magic takes ~20 minutes. You'll get an email when its ready!
      </p>
      <img
        src="~/assets/img/blur.png"
        alt="AI Headshot blur"
        class="rounded-lg object-cover w-full md:w-3/4 lg:w-1/2 mx-auto"
      />
    </div>

    <!-- Step 3: Generate images -->
    <div class="space-y-4">
      <div class="flex items-center justify-center space-x-4">
        <div
          class="text-3xl font-bold text-blue-600 bg-white border-2 border-blue-600 rounded-full w-10 h-10 flex items-center justify-center"
        >
          3
        </div>
        <h3 class="text-2xl font-semibold">Get amazing headshots</h3>
      </div>
      <p class="text-sm text-gray-600 text-center">
        Once your model is trained, we'll give you amazing headshots!
      </p>
      <img
        src="~/assets/img/result.png"
        alt="AI Headshot result"
        class="rounded-lg object-cover w-full md:w-3/4 lg:w-1/2 mx-auto"
      />
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped></style>
