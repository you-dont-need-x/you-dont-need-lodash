# You Don't Need Lodash

"You Don't Need Lodash" is intened to show how modern javascript can replace most of the Lodash library.

### It's 2018; Things Have Changed

**9+ years after Lodash's initial release, the browser landscape has drastically changed.**
The purpose of this is not to tell you that you shouldn't use Lodash, but rather to re-educate you on what exactly Lodash is useful for. The JavaScript standard library, and other browser APIs, have been much better standardized, and many of the previous pitfalls of compatibility no longer exist. While Lodash is still useful, it is less so than before, and it's important for you--the developer--to be familiar with the underlying APIs that libraries are abstracting.
A lot of the new APIs and methodologies are much easier to understand, and are sometimes more coherent than those in libraries like Lodash.

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

## \_.compact(array)

**Lodash**

```javascript
_.compact([0, 1, false, 2, "", 3]);
```

**Modern** | Using [Array.filter](http://devdocs.io/javascript/global_objects/array/filter) and [Arrow functions](http://devdocs.io/javascript/functions/arrow_functions)

```javascript
[0, 1, false, 2, "", 3].filter(element => element);
```

---

## \_.concat(array, [values])

**Lodash**

```javascript
const array = [1];
const other = _.concat(array, 2, [3], [[4]]);
```

**Modern** | Using [Array.concat](http://devdocs.io/javascript/global_objects/array/concat)

```javascript
const array = [1];
const other = array.concat(2, [3], [[4]]);
```

---

## \_.drop(array, [n=1])

**Lodash**

```javascript
_.drop([1, 2, 3], 2);
```

**Modern** | Using [Array.slice](http://devdocs.io/javascript/global_objects/array/slice)

```javascript
[1, 2, 3].slice(2);
```

---

## \_.fill(array, value, [start=0], [end=array.length])

**Lodash**

```javascript
_.fill([4, 6, 8, 10], "*", 1, 3);
```

**Modern** | Using [Array.fill](http://devdocs.io/javascript/global_objects/array/fill)

```javascript
[4, 6, 8, 10].fill("*", 1, 3);
```

---
