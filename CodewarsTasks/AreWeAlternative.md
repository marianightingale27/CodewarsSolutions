Are we alternate?
=================

https://www.codewars.com/kata/are-we-alternate/train/javascript

```javascript
function isAlt(word){
  let arr = word.split('');
  let arrVowels = ['a', 'e', 'i', 'o', 'u'];
  let lastLetterIsVowel = arrVowels.includes(arr[0]);
  if(word.length == 1) return true;

    for(let i = 1; i < arr.length; i++){
      if (arrVowels.includes(arr[i]) === lastLetterIsVowel){
        return false;
      } else {
        lastLetterIsVowel = arrVowels.includes(arr[i]);
          if (i == arr.length -1){
            return true;
          }
      }
    }
}```