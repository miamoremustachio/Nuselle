- A parameter is the variable listed inside the parentheses in the function declaration _(it’s a declaration time term)_
- An argument is the value that is passed to the function when it is called _(it’s a call time term)_

If a function does not return a value, it is the same as if it returns `undefined`:

```jsx
function doNothing() { }
console.log( doNothing() === undefined ); // true
```

• Values passed to a function as parameters are _copied_ to its local variables:

```jsx
function screamify(text) {
  text = text + '!'; // change argument
}

let text = 'Howdy';

screamify(text); // Howdy!

console.log( text ); // Howdy
// the value of "text" is the same, the function modified only a local copy
```




[^1]: Sources:
	[https://javascript.info/function-basics](https://javascript.info/function-basics)
