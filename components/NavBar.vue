<template>
  <div class="flex w-full px-8 py-4 justify-between items-center border-b">
    <div class="flex gap-2 align-middle h-full">
      <NuxtLink to="/">
        <h2 class="font-bold">Headshots AI</h2>
      </NuxtLink>
    </div>
    <div class="flex gap-4 items-center">
      <NuxtLink v-if="!user" to="/login">
        <ButtonComponent class="">Login / Signup</ButtonComponent>
      </NuxtLink>

      <Menu v-else as="div" class="relative inline-block text-left">
        <div>
          <MenuButton
            class="inline-flex w-full justify-center gap-x-1.5 bg-white px-3 py-2 text-sm font-semibold text-gray-900ring-1 hover:bg-gray-50"
          >
            <UserCircleIcon class="text-gray-500 h-6" />
          </MenuButton>
        </div>

        <transition
          enter-active-class="transition ease-out duration-100"
          enter-from-class="transform opacity-0 scale-95"
          enter-to-class="transform opacity-100 scale-100"
          leave-active-class="transition ease-in duration-75"
          leave-from-class="transform opacity-100 scale-100"
          leave-to-class="transform opacity-0 scale-95"
        >
          <MenuItems
            class="absolute right-0 z-10 mt-2 w-56 origin-top-right divide-y divide-gray-100 rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
          >
            <div class="px-4 py-3">
              <p class="truncate text-sm font-medium text-gray-900">
                {{ user.email }}
              </p>
            </div>
            <div class="py-1">
              <MenuItem v-slot="{ active }">
                <button
                  type="submit"
                  :class="[
                    active ? 'bg-gray-100 text-gray-900' : 'text-gray-700',
                    'block w-full px-4 py-2 text-center text-sm',
                  ]"
                  @click="logout"
                >
                  Log out
                </button>
              </MenuItem>
            </div>
          </MenuItems>
        </transition>
      </Menu>
    </div>
  </div>
</template>

<script setup>
import { Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue';
import { UserCircleIcon } from '@heroicons/vue/24/solid';

const client = useSupabaseClient();
const user = useSupabaseUser();

const logout = async () => {
  await client.auth.signOut();
  navigateTo('/');
};
</script>

<style lang="scss" scoped></style>
