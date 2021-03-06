# deep-clone-fn

[![npm version](https://img.shields.io/npm/v/deep-clone-fn)](https://npmjs.com/package/deep-clone-fn)

A modification of Sindre Sorhus's excellent [mimic-fn](https://www.npmjs.com/package/mimic-fn) for deep cloning functions.

## Installation

```shell
npm install deep-clone-fn
```

## Usage

```typescript
import deepCloneFunction from 'deep-clone-fn';

function f(x) {
  return x;
}

f.myProperty = { foo: 'bar' };

const g = deepCloneFunction(f);

f.myProperty.foo = 'baz';

console.log(g.myProperty); // { foo: 'bar' }
console.log(g('foo')); // foo
```
