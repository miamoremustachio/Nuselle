## ✍️ Syntax

```jsx
function* generator() {
  yield 1;
  yield 2;
  yield 3;
}

const gen = generator();

console.log(gen.next().value); // 1
console.log(gen.next().value); // 2
console.log(gen.next().value); // 3
```

When generator function is called, it doesn’t run its code. Instead it returns a generator object to manage the execution.

## 🛠️ Methods

The main method of a generator is `next()`.

When called, it runs the execution until the nearest `yield` statement. Then the function execution pauses, and the yielded `value` is returned to the outer code.

The result of `next()` is always an object with two properties:

- `value`: the yielded value.
- `done`: `true` if the function code has finished, otherwise `false`.



[^1]: Sources:
	<https://javascript.info/generators>
	<https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator>
