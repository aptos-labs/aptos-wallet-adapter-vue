<script setup lang="ts">
interface LinkProps {
  href?: string;
}
defineProps<LinkProps>();
defineSlots<{
  default?(props: Record<string, never>): any;
  link?(props: Record<string, never>): any;
}>();
</script>

<template>
  <template v-if="$slots.default">
    <slot name="link" />
  </template>
  <template v-else>
    <a v-bind="$attrs" :href="href" target="_blank" rel="noopener noreferrer"
      >Privacy Policy</a
    >
  </template>
</template>
