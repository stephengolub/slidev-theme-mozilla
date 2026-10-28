<script setup lang="ts">
// Responsive card grid: <MozCards :cols="3"> <MozCard/> ... </MozCards>
withDefaults(defineProps<{ cols?: number; gap?: string }>(), { cols: 2, gap: '1.5rem' })
</script>

<template>
  <div class="moz-cards" :style="{ gridTemplateColumns: `repeat(${cols}, 1fr)`, gap }">
    <slot />
  </div>
</template>

<style scoped>
.moz-cards {
  display: grid;
  margin: 2rem auto 0;
  max-width: 1000px;
}
</style>
