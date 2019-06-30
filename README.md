

String average (6)
=========
https://www.codewars.com/kata/string-average/train/javascript

**Task:**

You are given a string of numbers between 0-9. Find the average of these numbers and return it as a floored whole number (ie: no decimal places) written out as a string. Eg:
"zero nine five two" -> "four"
If the string is empty or includes a number greater than 9, return "n/a"

**Solution:**
```javascript
function averageString(str){
  let arr = str.split(" ");
  let dic = ['zero', 'one', 'two', 'three', 'four', 'five', 'six', 'seven', 'eight', 'nine'];
  let sum = 0;
  for (let i = 0; i < arr.length; i++){
    if(dic.includes(arr[i])){
      sum += dic.indexOf(arr[i]);
    } else return 'n/a';
  } 
return dic[Math.floor(sum/arr.length)];
}```