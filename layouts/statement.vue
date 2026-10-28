<template>
  <div class="slidev-layout statement h-full grid place-content-center text-center">
    <div class="my-auto">
      <slot />
    </div>
  </div>
</template>

<style>
.statement h1 {
  font-size: 2.6em;
}
.statement h1 + p {
  margin-top: 1.5rem;
  font-size: 1.15em;
}
.slidev-layout.statement h1 + p > strong:only-child {
  color: var(--moz-accent);
}
</style>
