# core-code-from-scratch-readme
Week challenges (Tuesday) 05/04/2022

 1.Explanation about Interpreted And Compiled Programming Languages 
-Compiled means convert a whole code into machine language or binary code that the procesor can execute. For instance, is the traslation of the source code to machine code, performs some operations, check syntax, it optimises our code and generate a machine code and is executed faster.
-Interpreted run through a program line by line and execute each command. For instance, directly executes the source code the program line by line.

2. Is Java compiled or interpreted, or both?
-Java is both type, Java source code needs to be compiled into bytecode. And bytecode is a special machine language native to the JAVA also interpreted and executes this code at runtime.

3. Pseudocode Currency Coverter 
  1. START
  2. Dollars  <-- GET
  3. 0.000022  <-- BitCoinPrice GET
  4. ConvertedValue <-- Dollars * BitCoinPrice
  5. PRINT  ConvertedValue
  6. END
  
 
Wednesday 06/04/2022

1. Your date of birth in the matrix? exercise    110110101011100

2. MIPS exercise 
  .data
        Numero1 : .asciiz "\nIngresa numero 1:\n"
        Numero2 : .asciiz "\nIngresa numero 2:\n"
        Numero3 : .asciiz "\n EL resultado es:\n"
        
  .text
        main:
              li $v0, 4
              la $a0, Numero1
              syscall
              
              li $v0, 5
              syscall
              
              move $t0, $v0
              
              li $v0, 4
              la $a0, Numero2
              syscall
              
              li $v0, 5
              syscall
              
              move $t1, $v0
              
              add $t2, $t0, $t1
              
              li $v0, 4
              la $a0, Numero3
              syscall
               
              li $v0, 1
              move $a0, $t2
              syscall
              
  
Ingresa numero 1:
5

Ingresa numero 2:
7

 EL resultado es:
12
-- program is finished running (dropped off bottom) --


3. Display your name exercise

.data
	      my_name: .asciiz "\nMariel\n"
  .text
	      main:
              li $v0, 4
              la $a0, my_name
              syscall
	      
Thursday 07/04/2022	 
1. Print special numbers 1 to 100
var str = '';

for (var x = 0; x < 101; x++) {
  str = str + x;
}

console.log(str);

'0123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100'

2. Bad Code 

var cond = false;

if (cond) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
VM241:6 The cond variable is false

3. Bad Code 2

var n = 100;

if (n == 100) {
  console.log('This is a special number!');
}
else if (n < 1000 && n % 10 == 0) {
  console.log('This number is almost special');
}
else {
  console.log('Just a regular number');
}
VM781:4 This is a special number!



WEEK 2
TUESDAY 19/04
1. Multiply exercise


function multiply(a, b){
  return a * b
}

2. ASCII Total exercise

function uniTotal(str) {
  let count = 0;
  for (let i = 0; i < str.length; i++) {
    count += str.charCodeAt(i);
  }
  return count;
}



3. Char From ASCII Value exercise


function getChar(c){
 return String.fromCharCode(c)
}

getChar(5);



4. Binary Addition exercise

function addBinary(a,b) {
let sum = a + b;
  return sum.toString(2);
}


5. Student's Final Grade exercise

function finalGrade(exam, projects) {
  let total = 0;
  if (exam > 90 || projects > 10) {
  total = 100;
} else if (exam > 75 && projects >= 5) {
  total = 90;
} else if (exam > 50 && projects >= 2) {
  total = 75;
} else {
  total = 0;
}
  return total;
}



Wednesday 20/04

1. Holiday VIII - Duty Free exercise

function dutyFree(normPrice, discount, hol){
let descuentoTotal = normPrice*(discount/100);
 
  return Math.floor (hol/descuentoTotal);
}

2. Twice As Old exercise

function twiceAsOld(dadYearsOld, sonYearsOld) { n
  let dobAgeSon = 2*sonYearsOld;
  return Math.abs(dadYearsOld - dobAgeSon);
}

3. Valid Spacing exercise

function validSpacing(s) {
    if(/^[\s]/.test(s) == true || /[\s]$/.test(s) == true) { 
     return false;
  }
  
  for(let i = 0; i < s.length; i++) {
    if(s.charAt(i) === ' '){ 
      if(i != 0 && s.charAt(i-1) === ' ') {
        return false;
      }
      if(i != (s.length - 1) && s.charAt(i+1) === ' ') {
        return false;
      }
    }
  }
  
  return true; 
}



4. Fake Binary 


function fakeBin(x){
let digits = '';
    for (let i = 0; i < x.length; i++) {
      if (parseInt(x[i]) < 5){
        digits = digits + '0';
      } else {
        digits = digits + '1';
      }
    }
  return digits;
}



Thursday

1. Remove All Exclamation Marks From The End Of Sentence
 
function remove (str) {  
  const Regex = /!*$/g;
  return str.replace(Regex,'');
}

2. Vowel Remover 

function shortcut (string) {
  return string.replace(/[aeiou*]/g, '');
}


3. Rock Paper Scissors! 


const rps = (user1, user2) => {
  let result = "";
  if (user1 === user2) {
    result = "Draw!";
  }
  else if (user1 === "paper" && user2 === "rock") {
    result = "Player 1 won!";    
  }
  else if (user1 === "scissors" && user2 === "paper") {
    result = "Player 1 won!";
  }
  else if (user1 === "rock" && user2 === "scissors") {
    result = "Player 1 won!";
  }
  else if (user1 === "paper" && user2 === "scissors") {
    result = "Player 2 won!";    
  }
  else if (user1 === "scissors" && user2 === "rock") {
    result = "Player 2 won!";
  }
  else if (user1 === "rock" && user2 === "paper") {
    result = "Player 2 won!";
  }
  return result
} 




4. Persistent Bugger 


function persistence(num) {
  let counter = 0;
  
  let digits = num.toString().split(""); // 39 -> "39" -> ["3", "9"]
  
  while (digits.length > 1) {
    let results = 1;
    
    for (let i = 0; i < digits.length; i++){
      results = results * digits[i];
    }
    
    digits = results.toString().split("");
    
    counter = counter + 1;
  }
 
  return counter;
}



 WEEK 3
 
1. Who Likes It?  
  
 function likes(names) {
  if (names.length == 0) return 'no one likes this';
  if (names.length == 1) return names[0] + ' likes this';
  if (names.length == 2) return names[0] + ' and ' + names[1] + ' like this';
  if (names.length == 3) return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this';
  return (names[0] +', ' + names[1] + ' and ' + (names.length - 2) + ' others like this');
}




2. Bit Counting

var countBits = function(n) {
  const base = (n).toString(2).split('');
  const result = base.reduce((sum, num) => sum + Number(num), 0);

  return result;
};



3. Your Order, Please 

function order(words){
  return words.split(' ').sort(function(a, b){
      return a.match(/\d/) - b.match(/\d/);
   }).join(' ');
}  


Tuesday


1. Simple Pig Latin

function pigIt(str){
  let newArr = [];
  let strArr = str.split(" ")
  strArr.forEach(x => {
    let wordArr = x.split("")
    wordArr.push(wordArr[0], 'ay'), wordArr.shift()
    if (x === "!" || x === "?" || x === "." || x === "," || x === ";"){
      newArr.push(x)
    } else {
      newArr.push(wordArr.join(""))
    }    
  })
  return newArr.join(" ")
  
}



2. Counting Duplicates 

function duplicateCount(text){
  const splitString = text.toLowerCase().split("").sort();
  let results = [];

  for (let i = 0; i < splitString.length; i++) {
    if (splitString[i] === splitString[i + 1]) {
      results.push(splitString[i]);
    }
  }
  const setArray = new Set(results);
  return setArray.size;
}



3. Decode The Morse Code


decodeMorse = function(morseCode){
  morseCode = morseCode.trim();
  let refinedData = morseCode.split('   ');
  let result = [];
  
  for (let i = 0; i < refinedData.length; i++) {
    let temp = refinedData[i].split(' ');
    for (let j = 0; j < temp.length; j++) {
      if (MORSE_CODE[temp[j]]) {
        result.push(MORSE_CODE[temp[j]]);
      }
    }
    
    if (i !== refinedData.length - 1) {
    result.push(' ');
    }
  }
  return result.join('');
}


Wednesday

1. Valid Parentheses 

function validParentheses(parens) {
  let openNum = 0;
  for (let i = 0; i < parens.length; i++){
    if (parens[i] == "(") {
      openNum += 1;           
    } else {
      openNum -= 1;
    }
   
    if (openNum < 0){
      return false
    }    
  }
  if (openNum === 0){
    return true    
  } else {
    return false
  }
}



2.  Convert String To Camel Case 

function toCamelCase(str){
 let strArray;
  
  
  if (str === ""){
    return "";    
  }
  
  if (str.indexOf("-") !== -1){
    strArray = str.split("-")
  } else {
    strArray = str.split("_")
  }
  
  let ccString = strArray[0];
  
  for (let i = 1; i < strArray.length; i++){
    ccString += capitalize(strArray[i]);           
  }
  
  return ccString
  
  }
    
  let capitalize = (str) => {
    return str[0].toUpperCase() + str.slice(1);
   
}



3. Unique In Order 

var uniqueInOrder=function(iterable){
  let newArr = []
  for (i = 0; i < iterable.length; i++){
    if (iterable[i] != iterable[i+1]){
      newArr.push(iterable[i])      
    }    
  }  
  return newArr
}


Thursday

1. Fold an array

function foldArray(array, runs) {
  const r = [];
  const c = array.slice();
  while (c.length) r.push(c.pop() + (c.shift() || 0));
  return runs - 1 ? foldArray(r, runs - 1) : r;
}


2. Encrypt This! 

var encryptThis = function(str) {
 if(str === '') {return '';
    }else {
        let s = str.split(' ');
        let x = s.map(element => {
            let a = element.split('');
            a[0] = element.charCodeAt(0);
            [a[1], a[a.length - 1]] = [a[a.length - 1], a[1]];
            return a.join('');});
      return x.join(' ');
    }
}

