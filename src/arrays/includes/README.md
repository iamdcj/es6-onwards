# The `includes` Method

The `includes` method is an helper function which will return a `boolean` based on the presence/lack thereof of the value passed to the function.

---

## Primitives

The includes method is useful when working with primitive values;

### Numbers

If the array contains at least one member which a value matching that passed to the function, it will return `true`, else it will return `false`.

```
const numbers = [1, 2, 3, 4];

numbers.includes(3); // true

```

### Strings

If the array contains at least one member which a value matching that passed to the function, it will return `true`, else it will return `false`.

```
const strings = ["David", "Steffie", "Nole"];

strings.includes("Bob"); // false
```

## Composite

The `include` method isn't particularly useful when working with arrays containing compositive values, and something like the [`find`](../find) method might be a better candidate.

### Objects

If the `includes` method is used on a composite value like an `object`, it will _always_ return `false`; objects are passed by reference, not value.

```
const users = [{ user: "David" }, { user: "Steffie" }, { user: "Nole" }];

users.includes({ user: "Steffie" }); // false

```

## Useage

The `includes` helper can be used to create control flow when dealing with arrays; if an element is/isn't present then the application can progress/stop/return from a function.

```
const numbers = [1, 2, 3, 4];

if(numbers.includes(3)) {
  // ...do something
}
```
