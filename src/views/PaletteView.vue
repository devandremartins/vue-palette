<template>{{ palettes }}</template>

<script>
import palettes from '@/data/seedPalettes';

export default {
  name: 'PaletteView',

  data() {
    return {
      palettes,
    };
  },
};
</script>

<style scoped></style>
