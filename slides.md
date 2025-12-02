---
# Custom colorful layered theme
theme: default
layout: intro
# Enable PDF download
download: false
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Vibe Coding - Lesssons and Experiences
info: |
  ## A presentation for the BTrust Conference 2025
  By [Sandeep Ramgolam](https://github.com/MrSunshyne)
  Community at [coders.mu](https://coders.mu)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: view-transition
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
showSponsor: false
# open graph
seoMeta:
  # By default, Slidev will use ./og-image.png if it exists,
  # or generate one from the first slide if not found.
  ogImage: auto
  # ogImage: https://cover.sli.dev
---

# Vibe Coding
## Lessons and exeperiences


> A Presentation for the BTrust Dev Day 2025


<img src="/images/btrust-branding/Btrust-Dev-Day-black.png" class="w-32 object-fit" />


<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->
---
src: ./pages/intro/qr.md
hide: false
---

---
src: ./pages/intro/speaker-introduction.md
hide: false
---

---
src: ./pages/meetups/66/community.md
---

---
src: ./pages/meetups/66/gallery.md
---

---
src: ./pages/meetups/66/vibe.md
hide: false
---

---
src: ./pages/intro/speaker-find-me.md
hide: false
---