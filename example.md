---
theme: ./
title: Mozilla theme example
layout: cover
---

# Big idea.

## The punchline.

<template v-slot:meta>

Your Name · Mozilla

Event · Date · Room

</template>

---
layout: statement
---

# One bold claim

**The supporting line, in mint.**

---
layout: center
---

<MozEyebrow>Beyond the basics</MozEyebrow>

# A centered title

**Subtitle in body gray.**

---
layout: default
---

# Compare

<MozCards :cols="2">
  <MozCard title="Before" edge="left">

  - Thing one
  - Thing two

  </MozCard>
  <MozCard title="After" edge="left" variant="accent">

  - Better one
  - Better two

  </MozCard>
</MozCards>

---
layout: center
---

# Progression

<MozCards :cols="3">
  <MozCard title="Simple">Fast, fails on nuance</MozCard>
  <MozCard title="Semantic">Catches strategy</MozCard>
  <MozCard title="Advanced" variant="accent">Policy-aware</MozCard>
</MozCards>

---
layout: end
---

# Thank you.

**Questions? Find us at example.com.**
