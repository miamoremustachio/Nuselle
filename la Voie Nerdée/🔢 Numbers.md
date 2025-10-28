# JavaScript
## 🍧 Syntax

We can use underscore `_` as the separator:

```jsx
let billion = 1_000_000_000;
```

And `e` to shorten a number (it multiplies the number by 1 with the given zeroes count):

```jsx
let billion = 1e9;  // 1 billion, literally: 1 and 9 zeroes
alert( 7.3e9 );  // 7.3 billions (same as 7300000000 or 7_300_000_000)

1e3 === 1 * 1000; // e3 means *1000
1.23e6 === 1.23 * 1_000_000; // e6 means *1000000
```

A negative number after `e` means a division by 1 with the given number of zeroes:

```jsx
// -3 divides by 1 with 3 zeroes
1e-3 === 1 / 1000; // 0.001

// -6 divides by 1 with 6 zeroes
1.23e-6 === 1.23 / 1000000; // 0.00000123

// an example with a bigger number
1234e-2 === 1234 / 100; // 12.34, decimal point moves 2 times
```

To call a method directly on a number, we need to place two dots `..` after it:

```jsx
42..toString(16)

(123456).toString(36) // Alternative option
```

## 🧮 Numeral systems

|         | ***Decimal*** | ***Hexadecimal*** | ***Binary*** | ***Octal*** |
| ------- | ------------- | ----------------- | ------------ | ----------- |
| Prefix  |               | 0x                | 0b           | 0o          |
| Example | `255`         | `0xff`            | `0b11111111` | `0o377`     |

The method `num.toString(base)` returns a string representation of `num` in the numeral system with the given `base`:

```jsx
let num = 255;

console.log( num.toString(16) );  // ff
console.log( num.toString(2) );   // 11111111
```

## ⏺️ Rounding

### ⬇️ **Math.floor**

_Rounds down:_
`3.1` becomes `3`
`-1.1` becomes `-2`

### ⬆️ **Math.ceil**

_Rounds up:_
`3.1` becomes `4`
`-1.1` becomes `-1`

### ⭕ **Math.round**

_Rounds to the nearest integer:_
`3.1` becomes `3`
`3.6` becomes `4` 
`3.5` rounds up to `4` 
`-3.5` rounds up to `-3`

### ✂️ **Math.trunc**

_Removes anything after the decimal point without rounding:_
`3.1` becomes `3`
`-1.1` becomes `-1`

## Summary:

|      | **`Math.floor`** | **`Math.ceil`** | **`Math.round`** | **`Math.trunc`** |
| ---- | ---------------- | --------------- | ---------------- | ---------------- |
| 3.1  | 3                | 4               | 3                | 3                |
| 3.5  | 3                | 4               | 4                | 3                |
| 3.6  | 3                | 4               | 4                | 3                |
| -1.1 | -2               | -1              | -1               | -1               |
| -1.5 | -2               | -1              | -1               | -1               |
| -1.6 | -2               | -1              | -2               | -1               |

The method `toFixed(n)` rounds the number to `n` digits after the point and returns a string representation of the result:

```jsx
let num = 12.34;
console.log( num.toFixed(1) ); // "12.3"
```

This method is also useful as a workaround to imprecise calculations’ results.

## ⚗️ Parsing

To “read” a number from a string we can use `parseInt()` and `parseFloat()` functions:

```jsx
console.log( parseInt('100px') ); // 100
console.log( parseFloat('12.5em') ); // 12.5

console.log( parseInt('12.3') ); // 12, only the integer part is returned
console.log( parseFloat('12.3.4') ); // 12.3, the second point stops the reading

console.log( parseInt('a123') ); // NaN, the first symbol stops the process
```

## 🎷 Other

JavaScript has a built-in [Math](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Math) object which contains a small library of mathematical functions and constants:

### 🎲 **Math.random()**
Returns a random number from 0 to 1

### **Math.pow(n, power)**
Returns `n` raised to the given power

### **Math.max(a, b, c...)**
Returns the greatest from the arbitrary number of arguments.

### **Math.min(a, b, c...)**
Returns the smallest from the arbitrary number of arguments.

## 💧Increment/Decrement

### Prefix
returns the new value:

```jsx
let foo = 1;
let bar = ++foo;

console.log(bar); // 2
```

### Postfix
returns the old value:

```jsx
let foo = 1;
let bar = foo++;

console.log(bar); // 1
```



[^1]: Sources:
	[https://javascript.info/operators](https://javascript.info/operators#string-concatenation-with-binary)
	[https://javascript.info/number](https://javascript.info/number)


