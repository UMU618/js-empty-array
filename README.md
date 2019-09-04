# How do I empty an array in JavaScript? I choose = []

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

## Problem

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

Expect cases: 2nd loop, empty temp, won't empty arr.

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
