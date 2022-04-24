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
return String.fromCharCode(c);
}


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

WEEK 2 

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


