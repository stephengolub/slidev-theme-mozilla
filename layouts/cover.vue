<template>
  <div class="slidev-layout cover h-full flex flex-col justify-between">
    <img class="cover-logo" src="../assets/mozilla-symbol-white.svg" alt="Mozilla" />
    <div class="flex-1 flex flex-col justify-center">
      <slot />
    </div>
    <div class="cover-meta">
      <slot name="meta" />
    </div>
  </div>
</template>

<style>
.cover {
  padding: 40px 60px;
  text-align: left;
}
.cover-logo {
  position: absolute;
  top: 40px;
  left: 60px;
  height: 64px;
}
.cover h1 {
  font-size: 48px;
  margin: 0 0 12px;
}
.cover h2 {
  font-size: 32px;
  margin: 0;
}
.cover-meta p {
  margin: 12px 0 0;
  font-size: 14px;
  color: var(--moz-text-body);
}
.cover-meta p:last-child {
  font-size: 12px;
  color: var(--moz-text-muted);
}
</style>
