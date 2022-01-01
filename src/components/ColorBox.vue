<template>
  <div class="color-box" :style="{ background: color.hex }">
    <button @click="copyColor">COPY</button>
    {{ color.name }}
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'ColorBox',

  props: {
    color: Object,
  },

  methods: {
    copyColor() {
      navigator.clipboard.writeText(this.color.hex).then(
        function () {
          console.log('clipboard successfully set');
        },
        function () {
          console.log('clipboard write failed');
        },
      );
    },
  },
});
</script>

<style scoped>
.color-box {
  display: inline-block;
  width: 20%;
  height: 25%;
}
</style>
