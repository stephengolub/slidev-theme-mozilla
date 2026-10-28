<script setup lang="ts">
// A QR image with a mint label and a muted URL beneath it.
defineProps<{ src: string; label?: string; url?: string; size?: number }>()
</script>

<template>
  <div class="moz-qr">
    <img :src="src" :style="{ width: `${size ?? 200}px` }" />
    <p v-if="label" class="moz-qr-label">{{ label }}</p>
    <p v-if="url" class="moz-qr-url">{{ url }}</p>
  </div>
</template>

<style scoped>
.moz-qr {
  text-align: center;
}
.moz-qr img {
  margin: 0 auto;
}
.moz-qr-label {
  color: var(--moz-accent);
  font-size: 14px;
  font-weight: 600;
  margin-top: 1rem;
}
.moz-qr-url {
  color: var(--moz-text-body);
  font-size: 12px;
  margin-top: 0.25rem;
}
</style>
