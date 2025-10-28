An empty object can be created using one of two syntaxes:

```jsx
let user = new Object(); // "object constructor" syntax
let user = {};  // "object literal" syntax
```

## 📃 Computed properties

```jsx
let fruit = prompt("Which fruit to buy?", "apple");

let bag = {
	*[fruit]: 5, // the name of the property is taken from the variable fruit*
};

console.log( bag.apple ); // 5
```

The meaning of a computed property is simple: `[fruit]` means that the property name should be taken from `fruit`.

## ✍️ Property value shorthand

The use-case of making a property from a variable is so common, that there’s a special _property value shorthand_ to make it shorter.

```jsx
function makeUser(name, age) {
	*return {
    name, // same as name: name
    age,  // same as age: age
    // ...
  };*
}
```

## 📥 In operator

With `in` operator we can easily test whether the property exists:

```jsx
let user = { name: "John", age: 30 };

console.log( "age" in user ); // true
console.log( "blabla" in user ); // false
```

## 🔢 Properties order

Object is ordered “in a special fashion”: integer properties are sorted, others appear _in creation order_:

```jsx
let codes = {
  "49": "Germany",
  "41": "Switzerland",
  "44": "Great Britain",
  // ...
  "1": "USA"
};

for (let code in codes) {
	console.log(code); // 1, 41, 44, 49
}
```

## 🎌 Copying

Primitive values are always copied _“as a whole value”_, whereas objects are stored and copied _“by reference”._

Here we put a copy of `message` into `phrase`:

```jsx
let message = "Hello!";
let phrase = message;
```

As a result we have two independent variables, each one storing the string `"Hello!"`
![[Screenshot 2024-09-08 092711.png]]

Objects are not like that.

> **A variable assigned to an object stores not the object itself, but its “address in memory” – in other words “a reference” to it.**

Let’s look at an example of such a variable:

```jsx
let user = {
	name: "John"
};
```

![[Screenshot 2024-09-08 093006.png]]


> **When an object variable is copied, the reference is copied, but the object itself is not duplicated.**

For instance:

```jsx
let user = {
	name: "John"
};

let admin = user; // copy the reference
```

Now we have two variables, each storing a reference to the same object:
![[Screenshot 2024-09-08 093352.png]]

As you can see, there’s still one object, but now with two variables that reference it.

> **Two objects are equal only if they are the same object.**

## 🧬 Cloning

To perform a simple object cloning (create a “shallow copy”) we can use `Object.assign`:

```jsx
Object.assign(dest, ...sources);
```

- The first argument `dest` is a target object.
- Further arguments is a list of source objects.

For a deep cloning we can use `structuredClone()` method:

```jsx
let user = {
  name: "John",
  sizes: {
    height: 182,
    width: 50
  }
};

let clone = structuredClone(user);

console.log( user.sizes === clone.sizes ); // false, different objects

// user and clone are totally unrelated now
user.sizes.width = 60;    // change a property from one place
alert(clone.sizes.width); // 50, not related
```



[^1]: Sources:
	[https://javascript.info/object](https://javascript.info/object)
	[https://javascript.info/object-copy](https://javascript.info/object-copy)


