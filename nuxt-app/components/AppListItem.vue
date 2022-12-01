<script setup>
defineProps({
  brand: {
    type: Boolean,
    default: false,
  },
});
</script>
<template>
  <li :class="brand ? 'text-slate-500' : 'text-slate-900'"><slot></slot></li>
</template>