Initialize my name
==================
####Some people just have a first name; some people have first and last names and some people have first, middle and last names.
You task is to initialize the middle names (if there is any).

```javascript
function initializeNames(name){
  let arr = name.split(' ');
  let res = '';
  if(arr.length <= 2) return name;  
  for(let i = 1; i < arr.length-1; i++){
    res += arr[i][0] + '. '; 
  }
  return arr[0] + ' ' + res + arr[arr.length-1]; 
}


