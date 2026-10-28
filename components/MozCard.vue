<script setup lang="ts">
// variant: "plain" (gray), "accent" (mint, highlighted)
// edge:    "box" (full border, 8px radius) or "left" (4px left rule, as in comparisons)
withDefaults(defineProps<{ title?: string; variant?: 'plain' | 'accent'; edge?: 'box' | 'left' }>(), {
  variant: 'plain',
  edge: 'box',
})
</script>

<template>
  <div class="moz-card" :class="[`is-${variant}`, `edge-${edge}`]">
    <div v-if="title" class="moz-card-title">{{ title }}</div>
    <div class="moz-card-body"><slot /></div>
  </div>
</template>

<style scoped>
.moz-card {
  padding: 1.5rem;
  background: var(--moz-surface);
  text-align: left;
}
.edge-box {
  border: 1px solid var(--moz-border);
  border-radius: var(--moz-radius);
}
.edge-left {
  border-left: 4px solid var(--moz-text-muted);
  border-radius: var(--moz-radius-sm);
}
.is-accent {
  background: var(--moz-surface-accent);
}
.edge-box.is-accent {
  border: 2px solid var(--moz-accent);
}
.edge-left.is-accent {
  border-left-color: var(--moz-accent);
}
.moz-card-title {
  font-weight: 600;
  font-size: 1.1rem;
  margin-bottom: 0.75rem;
  color: var(--moz-text);
}
.is-accent .moz-card-title {
  color: var(--moz-accent);
}
.moz-card-body {
  font-size: 0.9rem;
}
.moz-card-body :deep(ul) {
  margin: 0;
  padding-left: 1.5rem;
  line-height: 1.8;
}
</style>
