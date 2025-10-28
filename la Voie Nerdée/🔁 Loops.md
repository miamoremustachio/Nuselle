## Breaking

- `break`
    Stops the loop immediately, passing control to the first line after the loop.
    
    The combination “infinite loop + `break` as needed” is great for situations when a loop’s condition must be checked in the middle of its body.


- `continue` 
    A “lighter version” of `break`.
    
    It doesn’t stop the whole loop — Instead, it stops the current iteration and forces the loop to start a new one.

## Labels

To break the outer loop inside inner loop we can use _labels:_

```jsx
labelName: for (let i = 0; i < 3; i++) {

  for (; j < 3; j++) {

	if (!j) break labelName; // breaks the outer "for" loop

    // do something...
  }
}
```

The `continue` directive can also be used with a label.



[^1]: Sources:
	[https://javascript.info/while-for](https://javascript.info/while-for)

### Bonus: the Blessed mnemonic
![[photo_2023-09-04_22-06-58.jpg]]

