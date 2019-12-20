# Solved-tasks
#### Be Concise I - The Ternary Operator
```javascript
function describeAge(a) {
  let s="You're a(n) ";
  return (a<=12) ? s+'kid': (a<=17) ? s+"teenager": (a<=64) ? s+"adult": s+"elderly";
}
```
#### Can we divide it?
```javascript
function isDivideBy(number, a, b) {
       return (number % a === 0 && number % b === 0);
     }
```
#### Switch it Up!
```javascript
function switchItUp(number){
let result;
switch(number) {
case 0:
  result = "Zero";
  break;
case 1:
  result = "One";
  break;
case 2:
  result = "Two";
  break;
case 3:
  result = "Three";
  break;
case 4:
  result = "Four";
  break;
case 5:
  result = "Five";
  break;
case 6:
  result = "Six";
  break;
case 7:
  result = "Seven";
  break;
case 8:
  result = "Eight";
  break;
case 9:
  result = "Nine";
  break;
}
return result;
}
```
#### Draw stairs
```javascript
function drawStairs(n) {
 let s = '';
 for (let i = 1; i < n; i++) {
  s+= "I\n";
     for (let j = 1; j <= i; j++) {
       s+= ' ';
      }
  }
  s+="I";
  return s;
}
```
#### Squares sequence
```javascript
function squares(x, n) {
if (n <= 0) return [];
let arr = new Array(n);
arr[0] = x;
for (let i = 1; i < n; i++) {
  arr[i] =  Math.pow(arr[i-1], 2);  
 }
return arr;
}
```
#### Find the next perfect square!
```javascript
function findNextSquare(sq) {
 if (Math.sqrt(sq) % 1 !== 0)  return -1;
 return (Math.sqrt(sq) + 1) ** 2;
}
```
#### Enumerable Magic #3 - Does My List Include This?
```javascript
function include(arr, item){
  for (let i = 0; i < arr.length; i++) {
   if (arr[i] === item) return true;
    }
    return false;
}
```