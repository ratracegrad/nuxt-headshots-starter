<template>
  <div
    class="flex-1 flex flex-col w-full px-8 sm:max-w-md justify-center gap-2"
  >
    <form
      class="flex-1 flex flex-col w-full justify-center gap-2"
      @submit.prevent="signInWithOtp"
    >
      <div class="rounded-xl border bg-card text-card-foreground shadow">
        <div class="flex flex-col space-y-1.5 p-6">
          <h3 class="font-semibold leading-none tracking-tight">
            Log In / Sign Up
          </h3>
          <p class="text-sm text-muted-foreground">
            Log into your account or sign up for a new one to get started.
          </p>
        </div>
        <div class="p-6 pt-0 grid gap-4">
          <label
            class="font-medium peer-disabled:cursor-not-allowed peer-disabled:opacity-70 text-md"
            for="email"
          >
            Email
          </label>
          <input
            class="rounded-md px-4 py-2 bg-inherit border"
            name="email"
            type="email"
            placeholder="you@example.com"
            required
            v-model="email"
          />
          <ButtonComponent
            class="bg-primary text-white shadow hover:bg-primary/90 h-9 px-4 py-2"
            @click="signInWithOtp"
            >Continue</ButtonComponent
          >
        </div>
        <div class="flex items-center p-6 pt-0">
          <p class="text-sm">
            By signing up, you agree to our
            <a href="#" class="underline"> Terms of Service </a>
            and
            <a href="#" class="underline"> Privacy Policy </a>
            .
          </p>
        </div>
      </div>
    </form>
  </div>
</template>

<script setup>
const supabase = useSupabaseClient();

const loading = ref(false);
const email = ref('');

const signInWithOtp = async () => {
  const { error } = await supabase.auth.signInWithOtp({
    email: email.value,
    options: {
      emailRedirectTo: 'http://localhost:3000/confirm',
    },
  });
  if (error) console.log(error);
};
</script>

<style lang="scss" scoped></style>
