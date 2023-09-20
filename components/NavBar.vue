<template>
  <div class="flex w-full px-8 py-4 justify-between items-center border-b">
    <div class="flex gap-2 align-middle h-full">
      <NuxtLink to="/">
        <h2 class="font-bold">Headshots AI</h2>
      </NuxtLink>
    </div>
    <div class="flex gap-4 items-center">
			<NuxtLink to="/login">
				 <ButtonComponent class="">Login / Signup</ButtonComponent>
			</NuxtLink>
     
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
