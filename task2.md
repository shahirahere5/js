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
const { name } = user;
const [a, b] = arr;
Spread / Rest
const newArr = [...arr, 4];
function sum(...nums) {}
Optional Chaining
user.profile?.email;
3. Iterators & Generators
Iterator

Object with next() returning { value, done }.

Generator
function* gen() {
  yield 1;
  yield 2;
}

yield pauses execution.

4. ES Modules vs CommonJS
ES Modules
import x from "./file.js";
export const a = 1;
CommonJS
const x = require("./file");
module.exports = {};

ESM is modern, static, supports tree-shaking.
