<script setup lang="ts">
defineSlots<{
  default?(props: Record<string, never>): any;
  disclaimer?(props: Record<string, never>): any;
}>();
</script>

<template>
  <template v-if="$slots.default">
    <slot name="disclaimer" />
  </template>
  <template v-else>
    <span v-bind="$attrs"> By continuing, you agree to Aptos Labs' </span>
  </template>
</template>
