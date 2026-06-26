1. Prototype Chain

Objects inherit from other objects via [[Prototype]].

JS looks up properties like this:

object → prototype → prototype’s prototype → null
```javascript
const animal = { eats: true };
const dog = { barks: true };
dog.__proto__ = animal;

dog.eats; // true
```

2. ES6+ Features

Destructuring
```javascript
const { name } = user;
const [a, b] = arr;
```


Spread / Rest
```javascript
const newArr = [...arr, 4];
function sum(...nums) {}
```

Optional Chaining
```javascript
user.profile?.email;
```

3. Iterators & Generators

Iterator

Object with next() returning { value, done }.

Generator
```javascript
function* gen() {
  yield 1;
  yield 2;
}
```
yield pauses execution.

4. ES Modules vs CommonJS

ES Modules
```javascript
import x from "./file.js";
export const a = 1;
```
CommonJS
```javascript
const x = require("./file");
module.exports = {};
```

ESM is modern, static, supports tree-shaking.
