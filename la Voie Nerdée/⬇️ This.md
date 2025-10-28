The value of `this` is evaluated during the run-time, depending on the context.

```jsx
let user = { name: "John" };
let admin = { name: "Admin" };

function sayHi() {
  alert( this.name );
}

// use the same function in two objects
user.f = sayHi;
admin.f = sayHi;

user.f(); // John  (this == user)
admin.f(); // Admin  (this == admin)
```

If there’s `this` inside a function, it expects to be called in an object context.

## Arrow functions have NO “this”

If we reference `this` from such a function, it’s taken from the outer “normal” function:

```jsx
let user = {
  name: "Oleg",
  sayHi() {
    let arrow = () => console.log(this.name);
    arrow();
  }
};

user.sayHi(); // Oleg
```



[^1]: Sources:
	[https://javascript.info/object-methods](https://javascript.info/object-methods)
