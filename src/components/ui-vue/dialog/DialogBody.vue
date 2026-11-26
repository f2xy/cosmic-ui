<script setup lang="ts">
import { twMerge } from "tailwind-merge";

const { class: className } = defineProps<{ class?: string }>();
</script>

<template>
  <div class="mt-4 flex min-h-0 flex-col border-y border-primary/30 bg-background/25">
    <div
      :class="
        twMerge([
          'flex min-h-0 flex-col gap-4 overflow-y-auto py-5 [mask-image:linear-gradient(to_bottom,transparent,black_1.25rem,black_calc(100%-1.25rem),transparent)]',
          className,
        ])
      "
    >
      <slot />
    </div>
  </div>
</template>
