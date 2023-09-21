<template>
  <div
    class="flex-1 flex flex-col w-full px-8 sm:max-w-md justify-center gap-2"
  >
    <form
      class="flex-1 flex flex-col w-full justify-center gap-2"
      @submit.prevent="signup"
    >
      <div class="rounded-xl border bg-card text-card-foreground shadow">
        <!-- card header -->
        <div class="flex flex-col space-y-1.5 p-6">
          <!-- card title -->
          <div class="font-semibold leading-none tracking-tight">Sign Up</div>
          <!-- card description -->
          <div class="text-sm text-muted-foreground">
            Sign up for a new account to get started.
          </div>
        </div>
        <!-- card content -->
        <div class="p-6 pt-0 grid gap-4">
          <label
            class="text-md font-medium leading-none peer-disabled:cursor-not-allowed peer-disabled:opacity-70"
            for="email"
          >
            Email
          </label>
          <input
            class="rounded-md px-4 py-2 bg-inherit border"
            name="email"
            type="email"
            placeholder="you@example.com"
            autocomplete="email"
            id="email"
            required
            v-model="email"
          />
        </div>
        <div class="p-6 pt-0 grid gap-4">
          <label
            class="text-md font-medium leading-none peer-disabled:cursor-not-allowed peer-disabled:opacity-70"
            for="password"
          >
            Password
          </label>
          <input
            class="rounded-md px-4 py-2 bg-inherit border"
            name="password"
            type="password"
            placeholder="you@example.com"
            autocomplete="new-password"
            id="new-password"
            required
            v-model="password"
          />
        </div>
        <div class="p-6 pt-0 grid gap-4">
          <ButtonComponent
            class="bg-primary text-white shadow hover:bg-primary/90"
            @click="signup"
            >Continue</ButtonComponent
          >
        </div>

        <!-- card footer -->
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
// const client = useSupabaseClient();

const email = ref('');
const password = ref(null);
const errorMsg = ref(null);
const successMsg = ref(null);

async function signup() {
  console.log('hello world');
  // try {
  // 	client.auth.signUp({
  // 		email: email.value,
  // 		password: password.value,
  // 	})
  // } catch (error) {

  // }
}
</script>

<style lang="scss" scoped></style>
