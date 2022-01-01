<template>
  <div class="palette-view">
    <ColorBox v-for="color in palette" :key="color.name" :color="color" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import palettes from '@/data/seedPalettes';
import ColorBox from '@/components/ColorBox.vue';

export default defineComponent({
  name: 'PaletteView',

  components: {
    ColorBox,
  },

  data() {
    return {
      palette: palettes[0].colors,
    };
  },
});
</script>

<style scoped>
.palette-view {
  height: 100vh;
}
</style>
