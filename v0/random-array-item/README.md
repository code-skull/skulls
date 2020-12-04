# Task: Find a random item in an `Array`

## Terminology
- Primitive value types: Number, Array 
- Terminology: random, integer, array item

## Prerequisites
`myArray`: an `Array` of items:

    ```js
    const myArray = ['one', 'two', 'three'];
    ```

    Or replace this with one of your own or one from another exercise.

## TLDR; Optimized Solution

```js
const myItem = myArray[Math.floor(Math.random() * myArray.length)];
```

## Brute Force Solution

```js
const length = myArray.length;
const randNumber = Math.random();
const arrayRatio = randNumber * length;
const lowInteger = Math.floor(arrayRatio);
const myItem = myArray[lowInteger];
```

## Walk-through
1. Find the length of an array with [`Array.prototype.length`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length):

    ```js
    const length = myArray.length;
    ```

2. Create a random `Number` between 0 and 1 with [`Math.random()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random):

    ```js
    const randNumber = Math.random();
    ```

3. Take a ratio of `myArray`'s length by multiplying it by `randNumber`. Once this `Number` is rounded down in the next step, we'll have the index of an item in `myArray`.

    ```js
    const arrayRatio = length * randNumber;
    ```

4. Round a `Number` down to its largest integer with [Math.floor](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/floor):

    ```js
    const lowInteger = Math.floor(arrayRatio);
    ```

5. Find an item in an array with an integer using bracket notation:

    ```js
    const myItem = myArray[lowInteger];
    ```

## Optimized Solution

```js
const myItem = myArray[Math.floor(Math.random() * myArray.length)];
```

