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

Wrong cases:

```js
// Wrong:
temp.splice(0, temp.length)
```

```js
// Wrong:
temp.length = 0
```

```js
// Wrong:
temp.length = 0
temp.length = 0
```

```js
// Wrong:
temp.splice(0, temp.length)
temp = []
```

```js
// Wrong:
temp.length = 0
temp = []
```

Right cases:

```js
// Right:
temp = []
```

```js
// Right:
temp = []
temp.splice(0, temp.length)
```

```js
// Right:
temp = []
temp.length = 0
```
