# [Compare Anything](https://dev.to/rasaf_ibrahim/compare-anything-in-javascript-with-just-a-function-5g1a)

A function that can compare not only strings, numbers, and booleans but also arrays and objects.

```javascript
function compareAnything (first, second) {
  /* Checking if any arguments are null */
  if(first === null || second === null) return false

  /* Checking if the types and values of the two arguments are the same. */
  if(first === second) return true

  /* Checking if any argument is none object */
  if(typeof first !== 'object'  || typeof second !== 'object') return false

  /* Using Object.getOwnPropertyNames() method to return the list of the objects’ properties */
  let first_keys = Object.getOwnPropertyNames(first)
  let second_keys = Object.getOwnPropertyNames(second)

  /* Checking if the objects' length are same*/
  if(first_keys.length !== second_keys.length) return false

  /* Iterating through all the properties of the first object with the for of method*/
  for(let key of first_keys) {
      /* Making sure that every property in the first object also exists in second object. */ 
      if(!Object.hasOwn(second, key)) return false
      /* Using the compareAnything function recursively (calling itself) and passing the values of each property into it to check if they are equal. */
      if (compareAnything(first[key], second[key]) === false) return false
  }
  /* if no case matches, returning true */ 
  return true
}
```
