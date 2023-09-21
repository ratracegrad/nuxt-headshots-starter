<template>
	<div>Waiting for login...</div>
</template>

<script setup>
const user = useSupabaseUser()
watch(user, () => {
  if (user.value) {
    return navigateTo('/overview')
  }
}, { immediate: true })
</script>

<style lang="scss" scoped>

</style>