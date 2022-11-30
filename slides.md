---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# background: bg.webp
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
# use UnoCSS
css: unocss
layout: image
image: bg.webp
---

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/anantoghosh" target="_blank" alt="GitHub"
    class="bg-gray-900 text-xl icon-btn !border-none text-white p-4 !hover:bg-gray-900">
    By Ananto Ghosh
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->
---

# Disability Types
- Visual
- Auditory
- Motor
  - [Controller](https://www.xbox.com/en-US/accessories/controllers/xbox-adaptive-controller)
- Cognitive
- Seizure and Vestibular Disorders


---

# What is ADA?

- The Americans with Disabilities Act (ADA) protects people with disabilities from discrimination.
- ADA is set of US Laws
- Under ADA is [Section 508](https://www.section508.gov/)

<!--
Here is another comment.
-->

---

# W3C, WIA, ARIA

- **W3C** develops open standards for the web.
  - HTML, SVG, CSS, Internationalization, Accessibility and more
- **W3C Web Accessibility Initiative** (WAI) develops standards and support materials to help you understand and implement accessibility.
  - WAI guidelines: Web Content Accessibility Guidelines (WCAG), Authoring Tool Accessibility Guidelines (ATAG), and User Agent Accessibility Guidelines (UAAG).
- **WCAG** are guidelines for creating accessible web content
- **Accessible Rich Internet Applications (ARIA)** supplements HTML, is a set of roles and attributes that define ways to make web content and web applications (especially those developed with JavaScript) more accessible to people with disabilities.
---

# WCAG

- [Quick Reference](https://www.w3.org/WAI/WCAG21/quickref/)
- WCAG 2.0
- WCAG 2.1
- Has 3 Levels - A, AA, AAA

---

# Which guideline/level to follow?

- Each country requires a guideline according to the law they have established
  - https://www.w3.org/WAI/policies/
- ADA Section 508 requires WCAG 2.0 Level AA Success Criteria
  - Organizations and businesses with 25 or more employees are subject to ADA, and those with 15 or more employees must comply with Section 508.

---

# How to check for compliance?

- https://accessibilityinsights.io/
- https://www.ibm.com/able/toolkit
- Chrome Lighthouse

---
layout: center
---

# Tips

---

# Use Semantic HTML first, ARIA second

https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles

```html
<article>
<aside>
<details>
<figcaption>
<figure>
<footer>
<header>
<main>
<mark>
<nav>
<section>
<summary>
<time>
```

---

# Use Semantic HTML first, ARIA second

```html
<header>
  <nav>
    <ul>
      <li><a href="page1">Page 1</li>
      <li><a href="page2">Page 2</li>
    </ul>
  </nav>
</header>
<article>
  <h1>How to be semantic</h1>
  <p>This is the description</p>
</article>
<aside>
  Sidebar content
</aside>
<footer>
  Footer content
</footer>
```

View example on accessiblitly tree viewer.

---

# ARIA roles


```html
<header> (banner)
  <nav> (navigation)
    <ul> (list)
      <li>(list-item) <a href="page1"> (link) Page 1</li>
      <li>(list-item) <a href="page2"> (link) Page 2</li>
    </ul>
  </nav>
</header>
<article> (article)
  <h1>How to be semantic</h1> (heading)
  <p>This is the description</p> (paragraph)
</article>
<aside> (complimentary)
  Sidebar content
</aside>
<footer> (contentinfo)
  Footer content
</footer>
```

https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles

Note: Instead of a `<div>` with an article role, use the `<article>` element. **Always use native element if available.**

---
layout: center
---

# Common Errors in the codebase

---
layout: center
---

# 1. Not using semantic elements
Page should have semantic meaning

---
layout: center
---

# 2. Incorrect tab-index

- Only vaild values for tabindex are 0 and -1.
- Don't use tabindex for native interactive elements.

https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/tabindex

---
layout: center
---

# 3. aria-label everywhere

- The aria-label attribute is intended for interactive elements only.
- aria-label must only be used when there is no appropriate text visible in the DOM that could be referenced as a label.

---
layout: center
---

# 4. Not using native elements (or ionic elements)

- Eg: ChallengeFeatureCard

---
layout: center
---

# 5. Using Nested interactive elements

- Eg: ChallengeFeatureCard

---
layout: center
---

# 6. Using roles with native elements

- Eg: ChallengeFeatureCard
---
layout: center
---

# End