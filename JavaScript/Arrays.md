# Arrays 

Here I am only going to talk about the 3 most important array methods which are *filter*, *map*, and *reduce*. 

1. *Filter*: Filter is an array method that filters an array based on a given condtion and returns a new array that pass the condtion. The filter method doesn't chage the older array. 

```javascript
arr = [1, 4, 5, 8, 10];
arr.filter(num => {
num % 2 === 0
});
console.log(arr);
// arr = [4, 8, 10]
```

2. *Map*: Map is an array method that applies a certian function to each element and returns a newer array.

```javascript
arr = [1, 2, 3, 4, 5];
arr.map(num => {
num = num + 2
});

consle.log(arr);
// arr = [3, 4, 5, 6, 7]
```

3. *Redcue*: Reduce as the name indicates it is a method that takes an array and reduces and returns a single value.

```javascript
arr = [ 1, 2, 3, 4];
arr.reduce(num => {
num =+ num
}, 0);

console.log(arr);
// arr = 10;
```
