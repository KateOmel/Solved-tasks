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