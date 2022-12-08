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
image: jest.png
# background: jest.png
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

# What is jest

- Jest is a popular JavaScript testing framework that is developed and maintained by [Simen Bekkhus](https://github.com/SimenB) at Facebook.
- Jest is built on top of the Jasmine testing framework and it uses the Jasmine test runner (now jest-circus with v29) to execute tests and generate test results.
- Jest is designed to be easy to set up and use, and it has a rich API that allows you to write tests for a wide range of scenarios, including unit tests, integration tests, and end-to-end tests.
- Jest has built-in support for snapshot testing and mocking, which makes it well-suited for testing React applications.
- Jest provides a number of additional features, such as code coverage reports and parallel test execution, that can help you improve the reliability and performance of your tests.

---

# What is jest

- Combination of
  - Test runner
  - Expect Library
  - Mocking library
  - Fake timer
  - Code Coverage
---

# React Testing Library

- It is maintained by a team of volunteers, led by Kent C. Dodds, and Sebastian Silbermann as a main contributer. It is widely supported and used by the React community.
- It is built on top of the official react-dom/test-utils library.
- It provides a more user-centric and intuitive API for testing React components.
- It provides utility functions for rendering components, finding elements in the rendered output, and simulating user events.
- It also provides utility functions for dealing with asynchronous updates to components.

By using the React Testing Library, you can write more reliable and maintainable tests for your React components. This can help you catch bugs and regressions in your code, and it can also help you improve the design and usability of your components.


---

# MSW

- MSW (Mock Service Worker) is a popular library for mocking HTTP requests in JavaScript.
- MSW allows you to easily mock HTTP requests and responses in your tests, so you can test your code without relying on a real network connection.
- It can mock different types of HTTP requests, such as GET, POST, PUT, and DELETE.
- It can also delay responses or throw errors, that can help you test more complex scenarios.

By using MSW, you can write more reliable and deterministic tests for your code that make HTTP requests.