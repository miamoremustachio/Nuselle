# JavaScript
When comparing values of different types, JavaScript converts the values to _numbers_.

**For a non-strict check** `==` there’s a special rule for `null` and `undefined`. These two are a “sweet couple”: they equal each other, but not any other value:

```jsx
console.log(null == undefined); // true
```

**For maths and other comparisons** they are converted to numbers:  `null` becomes `0`, while `undefined` becomes `NaN`.



[^1]: Sources:
	[https://javascript.info/comparison](https://javascript.info/comparison)
