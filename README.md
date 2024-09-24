# QA

## problem on input = [1, 2, 3, 4] output = [24, 12, 8, 6]
explanation: 2*3*4 = 24
1*3*4 = 12
1*2*4 = 8
1*2*3 = 6

```javascript
function getResArr(arr) {
  const result = [];
  
  for (let i = 0; i < arr.length; i++) {
    let mul = 1;
    for (let j = 0; j < arr.length; j++) {
      if (i !== j) {
        mul *= arr[j];
      }
    }
    
    result.push(mul);
  }
  
  return result;
}

console.log(getResArr([1, 2, 3, 4]));
```
