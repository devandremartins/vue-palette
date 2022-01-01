<template>
  <div class="palette-view">
    <ColorBox v-for="color in palette" :key="color.name" :color="color" />
  </div>
</template>

<script setup>
import palettes from '@/data/seedPalettes';
import ColorBox from '@/components/ColorBox.vue';

let palette = palettes[0].colors;
</script>

<style scoped>
.palette-view {
  height: 100vh;
}
</style>
