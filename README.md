[![License: Unlicense](https://img.shields.io/badge/license-Unlicense-blue.svg)](http://unlicense.org/)

# You Don't Need Lodash

"You Don't Need Lodash" is intended to show how modern javascript can replace most of the Lodash library.

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

**Modern** | Using [array.filter](http://devdocs.io/javascript/global_objects/array/filter) and [Arrow functions](http://devdocs.io/javascript/functions/arrow_functions)

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

**Modern** | Using [array.concat](http://devdocs.io/javascript/global_objects/array/concat)

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

**Modern** | Using [array.slice](http://devdocs.io/javascript/global_objects/array/slice)

```javascript
[1, 2, 3].slice(2);
```

---

## \_.fill(array, value, [start=0], [end=array.length])

**Lodash**

```javascript
_.fill([4, 6, 8, 10], "*", 1, 3);
```

**Modern** | Using [array.fill](http://devdocs.io/javascript/global_objects/array/fill)

```javascript
[4, 6, 8, 10].fill("*", 1, 3);
```

---

## \_.findIndex(array, [predicate=_.identity], [fromIndex=0])

**Lodash**

```javascript
const users = [
	{ user: "barney", active: false },
	{ user: "fred", active: false },
	{ user: "pebbles", active: true }
];

_.findIndex(users, o => o.user == "barney");
```

**Modern** | Using [array.findIndex](http://devdocs.io/javascript/global_objects/array/findindex)

```javascript
const users = [
	{ user: "barney", active: false },
	{ user: "fred", active: false },
	{ user: "pebbles", active: true }
];

users.findIndex(o => o.user == "barney");
```

---

## \_.head(array)

**Lodash**

```javascript
_.head([1, 2, 3]);
```

**Modern**

```javascript
[1, 2, 3][0];
```

---

## \_.flatten(array)

**Lodash**

```javascript
_.flatten([1, [2, [3, [4]], 5]]);
```

**New** | Using [array.flat](http://devdocs.io/javascript/global_objects/array/flat)

```javascript
[1, [2, [3, [4]], 5]].flat(1);
```

---

## \_.flattenDeep(array)

**Lodash**

```javascript
_.flattenDeep([1, [2, [3, [4]], 5]]);
```

**New** | Using [array.flat](http://devdocs.io/javascript/global_objects/array/flat)

```javascript
[1, [2, [3, [4]], 5]].flat(Infinity);
```

---

## \_.flattenDepth(array, [depth=1])

**Lodash**

```javascript
const array = [1, [2, [3, [4]], 5]];

_.flattenDepth(array, 1);
```

**New** | Using [array.flat](http://devdocs.io/javascript/global_objects/array/flat)

```javascript
const array = [1, [2, [3, [4]], 5]];

array.flat(1));
```

---

## \_.fromPairs(pairs)

**Lodash**

```javascript
_.fromPairs([["a", 1], ["b", 2]]);
```

**New** | Using [Object.fromEntries](https://github.com/tc39/proposal-object-from-entries)

```javascript
Object.fromEntries([["a", 1], ["b", 2]]);
```

---

## \_.indexOf(array, value, [fromIndex=0])

**Lodash**

```javascript
_.indexOf([1, 2, 1, 2], 2, 2);
```

**Modern** | Using [array.indexOf](http://devdocs.io/javascript/global_objects/array/indexof)

```javascript
[1, 2, 1, 2].indexOf(2, 2);
```

---

## \_.initial(array)

**Lodash**

```javascript
_.initial([1, 2, 3]);
```

**Modern** | Using [array.slice](http://devdocs.io/javascript/global_objects/array/slice)

```javascript
[1, 2, 3].slice(0, -1);
```

---

## \_.join(array, [separator=','])

**Lodash**

```javascript
_.join(["a", "b", "c"], "~");
```

**Modern** | Using [array.join](http://devdocs.io/javascript/global_objects/array/join)

```javascript
["a", "b", "c"].join("~");
```

---

## \_.last(array)

**Lodash**

```javascript
_.last([1, 2, 3]);
```

**Modern** | Using [array.slice](http://devdocs.io/javascript/global_objects/array/slice)

```javascript
[1, 2, 3].slice(-1)[0];
```

---

## \_.reverse(array)

**Lodash**

```javascript
const array = [1, 2, 3];

_.reverse(array);
```

**Modern** | Using [array.reverse](http://devdocs.io/javascript/global_objects/array/reverse)

```javascript
const array = [1, 2, 3];

array.reverse();
```

---

## \_.tail(array)

**Lodash**

```javascript
_.tail([1, 2, 3]);
```

**Modern** | Using [array.slice](http://devdocs.io/javascript/global_objects/array/slice)

```javascript
[1, 2, 3].slice(1);
```

---

## \_.take(array, [n=1])

**Lodash**

```javascript
_.take([1, 2, 3], 2);
```

**Modern** | Using [array.slice](http://devdocs.io/javascript/global_objects/array/slice)

```javascript
[1, 2, 3].slice(0, 2);
```

---

## \_.takeRight(array, [n=1])

**Lodash**

```javascript
_.takeRight([1, 2, 3], 2);
```

**Modern** | Using [array.slice](http://devdocs.io/javascript/global_objects/array/slice)

```javascript
[1, 2, 3].slice(-2);
```

---
