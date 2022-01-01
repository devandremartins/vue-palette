<template>
  <div class="color-box" :style="{ background: color.hex }">
    {{ color.name }}
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  color: Object,
});
</script>

<style scoped>
.color-box {
  display: inline-block;
  width: 20%;
  height: 25%;
}
</style>
