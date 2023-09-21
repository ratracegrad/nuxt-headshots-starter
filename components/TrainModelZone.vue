<template>
  <form class="rounded-md flex flex-col gap-8">
    <div class="space-y-2">
      <label
        class="text-sm font-medium leading-none peer-disabled:cursor-not-allowed peer-disabled:opacity-70"
        for="name"
      >
        Type
      </label>
      <p class="text-[0.8rem] text-muted-foreground">
        Give your model a name so you can easily identify it later.
      </p>
      <input
        class="rounded-md px-4 py-2 bg-inherit border max-w-screen-sm w-full"
        name="name"
        placeholder="e.g. Natalie Headshots"
        autoComplete="off"
        v-model="name"
      />
    </div>
    <div class="flex flex-col gap-4">
      <label
        class="text-sm font-medium leading-none peer-disabled:cursor-not-allowed peer-disabled:opacity-70"
        for="type"
      >
        Type
      </label>
      <p class="text-[0.8rem] text-muted-foreground">
        Select the type of headshots you want to generate.
      </p>

      <div
        role="radiogroup"
        aria-required="false"
        dir="ltr"
        class="grid grid-cols-3 gap-4"
        tabindex="0"
        style="outline: none"
      >
        <div>
          <button
            type="button"
            role="radio"
            aria-checked="true"
            data-state="checked"
            value="man"
            class="aspect-square h-4 w-4 rounded-full border border-primary text-primary shadow focus:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:cursor-not-allowed disabled:opacity-50 peer sr-only"
            id="man"
            aria-label="man"
            tabindex="-1"
          >
            <span data-state="checked" class="flex items-center justify-center">
              <svg
                width="15"
                height="15"
                viewBox="0 0 15 15"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="h-3.5 w-3.5 fill-primary"
              >
                <path
                  d="M11.4669 3.72684C11.7558 3.91574 11.8369 4.30308 11.648 4.59198L7.39799 11.092C7.29783 11.2452 7.13556 11.3467 6.95402 11.3699C6.77247 11.3931 6.58989 11.3355 6.45446 11.2124L3.70446 8.71241C3.44905 8.48022 3.43023 8.08494 3.66242 7.82953C3.89461 7.57412 4.28989 7.55529 4.5453 7.78749L6.75292 9.79441L10.6018 3.90792C10.7907 3.61902 11.178 3.53795 11.4669 3.72684Z"
                  fill="currentColor"
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                ></path>
              </svg>
            </span>
          </button>
          <input
            type="radio"
            aria-hidden="true"
            style="
              transform: translateX(-100%);
              position: absolute;
              pointer-events: none;
              opacity: 0;
              margin: 0px;
              width: 15.9844px;
              height: 15.9844px;
            "
            tabindex="-1"
            checked=""
            value="man"
          />
          <label
            class="text-sm font-medium leading-none peer-disabled:cursor-not-allowed peer-disabled:opacity-70 flex flex-col items-center justify-between rounded-md border-2 border-muted bg-transparent p-4 hover:bg-accent hover:text-accent-foreground peer-data-[state=checked]:border-primary [&amp;:has([data-state=checked])]:border-primary"
            for="man"
          >
            <svg
              stroke="currentColor"
              fill="currentColor"
              stroke-width="0"
              viewBox="0 0 192 512"
              class="mb-3 h-6 w-6"
              height="1em"
              width="1em"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M96 0c35.346 0 64 28.654 64 64s-28.654 64-64 64-64-28.654-64-64S60.654 0 96 0m48 144h-11.36c-22.711 10.443-49.59 10.894-73.28 0H48c-26.51 0-48 21.49-48 48v136c0 13.255 10.745 24 24 24h16v136c0 13.255 10.745 24 24 24h64c13.255 0 24-10.745 24-24V352h16c13.255 0 24-10.745 24-24V192c0-26.51-21.49-48-48-48z"
              ></path>
            </svg>
            Man
          </label>
        </div>
        <div>
          <button
            type="button"
            role="radio"
            aria-checked="false"
            data-state="unchecked"
            value="woman"
            class="aspect-square h-4 w-4 rounded-full border border-primary text-primary shadow focus:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:cursor-not-allowed disabled:opacity-50 peer sr-only"
            id="woman"
            aria-label="woman"
            tabindex="-1"
          ></button>
          <input
            type="radio"
            aria-hidden="true"
            style="
              transform: translateX(-100%);
              position: absolute;
              pointer-events: none;
              opacity: 0;
              margin: 0px;
              width: 15.9844px;
              height: 15.9844px;
            "
            tabindex="-1"
            value="woman"
          />
          <label
            class="text-sm font-medium leading-none peer-disabled:cursor-not-allowed peer-disabled:opacity-70 flex flex-col items-center justify-between rounded-md border-2 border-muted bg-transparent p-4 hover:bg-accent hover:text-accent-foreground peer-data-[state=checked]:border-primary [&amp;:has([data-state=checked])]:border-primary"
            for="woman"
          >
            <svg
              stroke="currentColor"
              fill="currentColor"
              stroke-width="0"
              viewBox="0 0 256 512"
              class="mb-3 h-6 w-6"
              height="1em"
              width="1em"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M128 0c35.346 0 64 28.654 64 64s-28.654 64-64 64c-35.346 0-64-28.654-64-64S92.654 0 128 0m119.283 354.179l-48-192A24 24 0 0 0 176 144h-11.36c-22.711 10.443-49.59 10.894-73.28 0H80a24 24 0 0 0-23.283 18.179l-48 192C4.935 369.305 16.383 384 32 384h56v104c0 13.255 10.745 24 24 24h32c13.255 0 24-10.745 24-24V384h56c15.591 0 27.071-14.671 23.283-29.821z"
              ></path>
            </svg>
            Woman
          </label>
        </div>
        <div>
          <button
            type="button"
            role="radio"
            aria-checked="false"
            data-state="unchecked"
            value="person"
            class="aspect-square h-4 w-4 rounded-full border border-primary text-primary shadow focus:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:cursor-not-allowed disabled:opacity-50 peer sr-only"
            id="person"
            aria-label="person"
            tabindex="-1"
            data-radix-collection-item=""
          ></button>
          <input
            type="radio"
            aria-hidden="true"
            style="
              transform: translateX(-100%);
              position: absolute;
              pointer-events: none;
              opacity: 0;
              margin: 0px;
              width: 15.9844px;
              height: 15.9844px;
            "
            tabindex="-1"
            value="person"
          />
          <label
            class="text-sm font-medium leading-none peer-disabled:cursor-not-allowed peer-disabled:opacity-70 flex flex-col items-center justify-between rounded-md border-2 border-muted bg-transparent p-4 hover:bg-accent hover:text-accent-foreground peer-data-[state=checked]:border-primary [&amp;:has([data-state=checked])]:border-primary"
            for="person"
          >
            <svg
              stroke="currentColor"
              fill="currentColor"
              stroke-width="0"
              viewBox="0 0 576 512"
              class="mb-3 h-6 w-6"
              height="1em"
              width="1em"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M268.3 32.7C115.4 42.9 0 176.9 0 330.2V464c0 8.8 7.2 16 16 16h32c8.8 0 16-7.2 16-16V320C64 186.8 180.9 80.3 317.5 97.9 430.4 112.4 512 214 512 327.8V464c0 8.8 7.2 16 16 16h32c8.8 0 16-7.2 16-16V320c0-165.3-140-298.6-307.7-287.3zm-5.6 96.9C166 142 96 229.1 96 326.7V464c0 8.8 7.2 16 16 16h32c8.8 0 16-7.2 16-16V320c0-74.8 64.5-134.8 140.8-127.4 66.5 6.5 115.2 66.2 115.2 133.1V464c0 8.8 7.2 16 16 16h32c8.8 0 16-7.2 16-16V320c0-114.2-100.2-205.4-217.3-190.4zm6.2 96.3c-45.6 8.9-76.9 51.5-76.9 97.9V464c0 8.8 7.2 16 16 16h32c8.8 0 16-7.2 16-16V320c0-17.6 14.3-32 32-32s32 14.4 32 32v144c0 8.8 7.2 16 16 16h32c8.8 0 16-7.2 16-16V320c0-59.2-53.8-106-115.1-94.1z"
              ></path>
            </svg>
            Unisex
          </label>
        </div>
      </div>

      <div
        class="rounded-md justify-center align-middle cursor-pointer flex flex-col gap-4 mt-3"
      >
        <label
          class="text-sm font-medium leading-none peer-disabled:cursor-not-allowed peer-disabled:opacity-70"
          for="type"
        >
          Samples
        </label>
        <p class="text-[0.8rem] text-muted-foreground">
          Upload 4-10 images of the person you want to generate headshots for.
        </p>
      </div>

      <div
        class="outline-dashed outline-2 outline-gray-100 hover:outline-blue-500 w-full h-full rounded-md p-4 flex justify-center align-middle"
      >
        <div className="flex justify-center flex-col items-center gap-2">
          <!-- <FaImages size="{32}" className="text-gray-700" /> -->
          <photo-icon class="text-gray-500 h-16" />
          <p className="self-center">
            Drag 'n' drop some files here, or click to select files.
          </p>
        </div>
      </div>
      <ButtonComponent type="submit" class="w-full bg-primary text-white hover:bg-primary/90" isLoading="{isLoading}">
        Train Model
      </ButtonComponent>
    </div>
  </form>
</template>

<script setup>
import { PhotoIcon } from '@heroicons/vue/24/solid';

const name = ref('');
</script>

<style lang="scss" scoped></style>
