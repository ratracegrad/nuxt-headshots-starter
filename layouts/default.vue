<template>
  <div class="min-h-screen flex flex-col">
    <section>
      <NavBar />
    </section>
    <main class="flex flex-1 flex-col items-center py-16">
      <slot />
    </main>
    <Footer></Footer>
  </div>
</template>
