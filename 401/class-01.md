# Node Ecosystem, TDD, CI/CD

## Array.map()

Array.map() method returns a new array with the same length as the original array with the results of calling a function for every array element, without mutating the original array.

### Syntax

`array.map((val, idx)=>{callback function})`


## Array.reduce()

- The reduce() method reduces the array to the values that match the callback function return (true or false) and store them in an accumulator, without mutating the original array.

### Syntax

`array.reduce((acc, val, idx)=>{callback function}, initVal)`

## Superagent

### With normal Promise .then() syntax

```javascript
function getData(){
 superagent.get(url).then(result =>{
    console.log(result.body)
})
}
```

###  with async / await syntax

```javascript
async function getData(){
    let result = await superagent.get(url);
    console.log(result);
}
```

## JavaScript Promises

A Promise in short has 3 states:

1. Pending: undefined
2. Fulfilled: a result value
3. Rejected: an error object

```javascript
let myPromise = new Promise(function(resolve, reject) {
  let x = 0;

// The producing code (this may take some time)

  if (x == 0) {
    resolve("OK");
  } else {
    reject("Error");
  }
});
```


## Are all callback functions considered to be Asynchronous? Why or Why Not?
No, not every callback considerred as asynchronous. for example the forEach consider as a callback function but not a asynchronous.