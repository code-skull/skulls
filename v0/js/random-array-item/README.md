# Task: Find a random item in an `Array`

This solution uses the built-in `Math` object to randomly generate an integer that falls within the first (`0`) and last (`length - 1`) index of an array.

## Topics Covered
- Primitive value types: `Number`, `Array`
- Built-in objects: [`Math.random()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random), [`Math.floor()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/floor)

## Prerequisites
- Some familiarity with [Javascript Basics](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps), specifically [Arrays](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Arrays).
- An `Array` of items:

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
1. Find the number of items in an array (its `length`) with [`Array.prototype.length`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length):

    ```js
    const length = myArray.length;
    ```

2. Create a random `Number` between 0 and 1 with [`Math.random()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random):

    ```js
    const randNumber = Math.random();
    ```

3. Multiply this random number by the length of `myArray` to scale it to the range of possible `myArray` indexes.

    ```js
    const scaledRatio = length * randNumber;
    ```

4. Round this number down to an integer with [`Math.floor`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/floor):

    ```js
    const lowInteger = Math.floor(arrayRatio);
    ```

5. Return the item in `myArray` that corresponds to the generated random integer:

    ```js
    const randItem = myArray[lowInteger];
    ```

## Brute Force Solution

```js
const length = myArray.length;
const randNumber = Math.random();
const scaledRatio = randNumber * length;
const lowInteger = Math.floor(scaledRatio);
const randItem = myArray[lowInteger];
```

## Optimized Solution

```js
const randItem = myArray[Math.floor(Math.random() * myArray.length)];
```
