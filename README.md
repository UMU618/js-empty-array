# How to empty an array in JavaScript?

When I write [pathfinding](https://blog.umu618.com/pathfinding/) codes in JavaScript, I ran into this problem: how to empty the array?

## Methods

- Method 1

```js
array = []
```

- Method 2

```js
array.length = 0
```

- Method 3

```js
array.splice(0, array.length)
```

- Method 4

```js
while (array.length > 0) {
    array.pop()
}
```

## Difference between Method 1 and the others

Method 1 only reassign a:

```
let a = [1, 2, 3]
let b = a

// empty a, but doesn't affect b
a = []

console.log('a =', a)
console.log('b =', b)
```

Method 2, 3, 4, will empty multiple variables referencing the same object:

```
let a = [1, 2, 3]
let b = a

// empty a and b
a.length = 0

console.log('a =', a)
console.log('b =', b)
```

## Example

See [index.htm](index.htm)

Unexpect cases: 2nd loop, arr === temp, empty temp, will empty arr.

```js
// Unexpect
temp.splice(0, temp.length)
```

```js
// Unexpect
temp.length = 0
```

```js
// Unexpect
temp.splice(0, temp.length)
temp.length = 0
```

```js
// Unexpect
temp.splice(0, temp.length)
temp = []
```

```js
// Unexpect
temp.length = 0
temp = []
```

Expect cases: 2nd loop, reassign temp, won't affect arr.

```js
// Expect
temp = []
```

```js
// Expect
temp = []
temp.splice(0, temp.length)
```

```js
// Expect
temp = []
temp.length = 0
```
