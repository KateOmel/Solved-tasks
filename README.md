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
#### Find the first non-consecutive number
```javascript
function firstNonConsecutive (arr) {
for (let i = 1; i < arr.length; i++) {
 if ( arr[i] === arr[i-1] + 1) { continue; }
 else return arr[i]; 
   }
   return null;
}
```
#### Remove the minimum
```javascript
function removeSmallest(numbers) {
  //throw "TODO: removeSmallest";
  let min = numbers[0];
  let index = 0;
  for (let i = 1; i < numbers.length; i++) {
   if ( numbers[i] < min) {
    min = numbers[i];
    index = i;
     }
  }
  let newArr = [];
  for (let i = 0; i < numbers.length; i++) {
   if ( i === index) continue;
   newArr.push(numbers[i]);
     }
  return newArr;
}
```
#### Pre-FizzBuzz Workout #1
```javascript
function preFizz(n) {
let arr = [];
for (let i = 1 ; i <= n; i++) {
arr.push(i);
}
return arr;
}
```
#### Two Oldest Ages
```javascript
// return the two oldest/oldest ages within the array of ages passed in.
function twoOldestAges(ages){
let arr = ages.sort( (a, b) => a - b);
return [arr[arr.length - 2], arr[arr.length - 1] ];
}
```
#### Mumbling
```javascript
function accum(s) {
s = s.toUpperCase();
let arr = s.split('');
	//console.log(arr);
  return arr.map( (el,i) => el += el.toLowerCase().repeat(i)).join('-');
  
}
```
#### Unique In Order
```javascript
var uniqueInOrder=function(iter){
if (iter === '') return [];
  let arr = [ iter[0] ];
  for (let i = 1; i < iter.length; i++) {
  if (iter[i] === iter[i-1]) continue;
  arr.push( iter[i] );
  }
  return arr;
}
```
#### Numbers to Letters
```javascript
function switcher(x){
let arr = [];
  for (let i = 0; i < 26; i++) {
  arr.push( String.fromCodePoint(97 + i) );
  }
  arr.reverse();
  arr.unshift(0);
  arr.push('!','?',' ');
  
  return x.map( el => arr[+el]).join('');
 
}
```
#### Thinking & Testing : Something capitalized
```javascript
function testit(s){
if (s === '') return '';
let arr = s.split(' ');
for (let i = 0; i< arr.length; i++) {
arr[i] = arr[i].split('');
arr[i][ arr[i].length -1] = arr[i][ arr[i].length -1].toUpperCase();
arr[i] = arr[i].join('');
}
return arr.join(' ');
}
```
#### Regex validate PIN code
````javascript
function validatePIN (pin) {
if (pin.length !== 4 && pin.length !== 6) return false;
  for (let i = 0; i < pin.length; i++) {  
  if (pin[i].codePointAt(0) > 47 && pin[i].codePointAt(0)< 58){
  continue; }
  else return false;
  }
  return true;
}
````
#### Get number from string
````javascript
function getNumberFromString(s) {
return +s.replace( /\D/g, '');
}
````
#### Replace all dots
```javascript
var replaceDots = function(str) {
return str.replace(/['.']/g, '-');
}
```
#### Exclamation marks series #2
```javascript
function remove(s){
while ( s[ s.length - 1] === '!') {
s = s.slice(0, -1); }
 return s;
}
```
#### Vowel remover
```javascript
function shortcut(string){
 return string.replace(/[a,e,i,o,u]/g, ''); 
 }
```
#### Can Santa save Christmas?
```javascript
function determineTime(durations){
let res = 0;
for (let i = 0; i < durations.length; i++) {
let arr = durations[i].split(':');
res += +arr[0]*60*60 + +arr[1]*60 + +arr[2];
 }
return res<= 24*60*60; 
}
```
#### Welcome
```javascript
function greet(language) {
let greeting = {
english: 'Welcome',
czech: 'Vitejte',
danish: 'Velkomst',
dutch: 'Welkom',
estonian: 'Tere tulemast',
finnish: 'Tervetuloa',
flemish: 'Welgekomen',
french: 'Bienvenue',
german: 'Willkommen',
irish: 'Failte',
italian: 'Benvenuto',
latvian: 'Gaidits',
lithuanian: 'Laukiamas',
polish: 'Witamy',
spanish: 'Bienvenido',
swedish: 'Valkommen',
welsh: 'Croeso',
};
return greeting[language] === undefined ? 'Welcome' : greeting[language];
}
```
#### arithmetic
```javascript
function arithmetic(a, b, operator){
  switch(operator) {
    case 'add':
      return a + b;
    case 'subtract':
      return a - b;
    case 'multiply':
      return a * b;
    case 'divide':
      return a / b;
  }
}
```
#### Job Matching #1
```javascript
function match(candidate, job) {
if (candidate.minSalary === undefined || job.maxSalary === undefined) return error;
  return 0.9*candidate.minSalary <= job.maxSalary;
}
```
#### Numbers to Objects
```javascript
function numObj(s){
let arr = [];
for (let i = 0; i < s.length; i++) {
let obj = {};
obj[s[i].toString()] = String.fromCharCode(s[i]);
arr.push(obj);
}
return arr;  
}
```
#### How many days are we represented in a foreign country?
```javascript
function daysRepresented(trips){
let arr = [];
for (let i = 0; i < trips.length; i++) {
for (let j = trips[i][0]; j <= trips[i][1]; j++) {
arr.push(j);
 }
}
arr = arr.filter( (el,i) => arr.indexOf(el) === i );
return arr.length;
}
```
#### Permute a Palindrome
```javascript
function permuteAPalindrome (input) { 
let obj = {};
let count = 0;
for (let i = 0; i < input.length; i++){
  
     if (obj[input[i]] === undefined) obj[input[i]] = 1;
     else obj[input[i]] += 1;
}
  
  for (let key in obj){
    if ( obj[key] % 2 === 0) continue;
    else count++;
  }  
 
  return count <= 1;
}
```
#### What is my name score? #1
```javascript
function nameScore(name){
let obj = {};
let score = 0;
  
  for (let i = 0; i < name.length; i++){  
    for (let key in alpha) {    
       if ( key.includes( name[i].toUpperCase()) ) score += alpha[key];     
    } 
  }
  obj[name] = score;
  return obj;
}
```
#### Most valuable character
```javascript
function solve(str) {
let arr = str.split('');
console.log(arr);
   let value = 0;
   const result = [];
   for (let i = 0; i < arr.length; i++){
     if ( value < arr.lastIndexOf(arr[i]) - arr.indexOf(arr[i]) ) 
       { value = arr.lastIndexOf(arr[i]) - arr.indexOf(arr[i])}
   }  
   for (let i = 0; i < arr.length; i++){
   if (arr.lastIndexOf(arr[i]) - arr.indexOf(arr[i]) === value) result.push(arr[i]);
   }
   return result.sort()[0];   
   }
```
#### The Office II - Boredom Score
```javascript
function boredom(staff){
let score = 0;
   let obj = {
accounts : 1,
finance : 2,
canteen : 10,
regulation : 3,
trading : 6,
change : 6,
IS : 8,
retail : 5,
cleaning : 4,
'pissing about' : 25, 
   }
for (let name in staff){
  if (obj[staff[name]] !== undefined) score += obj[staff[name]]; 
}
if (score <= 80) return 'kill me now';
else if ( score < 100) return 'i can handle this';
else return 'party time!!';
}
```
#### Is every value in the array an array?
```javascript
const arrCheck = value => {
for (let i = 0; i < value.length; i++){
if ( Array.isArray(value[i])  ) continue;
else return false;
}
return true;
}
```