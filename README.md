# You Don't Need Lodash

"You Don't Need Lodash" is intened to show how modern javascript can replace most of the Lodash library.

### It's 2018; Things Have Changed

**9+ years after Lodash's initial release, the browser landscape has drastically changed.**
The purpose of this is not to tell you that you shouldn't use Lodash, but rather to re-educate you on what exactly Lodash is useful for. The JavaScript standard library, and other browser APIs, have been much better standardized, and many of the previous pitfalls of compatibility no longer exist. While Lodash is still useful, it is less so than before, and it's important for you--the developer--to be familiar with the underlying APIs that libraries are abstracting.
A lot of the new APIs and methodologies are much easier to understand, and are sometimes more coherent than those in libraries like Lodash.

---

_[...]_ Please take a moment to consider if you actually need Lodash as a dependency; maybe you can include a few lines of utility code, and forgo the requirement. If you're only targeting more modern browsers, you might not need anything more than what the browser ships with.

_[...]_ Some developers believe that Lodash is protecting us from a great demon of browser incompatibility when, in truth, _[modern]_ browsers are pretty easy to deal with on their own.

---

Most of the APIs that I'll be showing can be [polyfilled](<https://en.wikipedia.org/wiki/Polyfill_(programming)>), meaning that if the browser is modern, and supports the APIs, it will use those, but if the browser is legacy, it will update the APIs with the new features, and allow all browsers to work.
**Modern features that can be polyfilled for legacy browsers:**

- Promise
- fetch
- classList
- Array.from
- Object.assign
- More...
  Although a couple of the modern examples have more characters in their code, they should not deter you from trying to understand these new APIs. Read carefully, and try to understand what the code is doing so that you can better reflect on whether or not you should use a library.

---
