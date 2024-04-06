1) Can you execute program with out making class as public?

Yes we can write programs without public class. when you compiled javac is going to generate .class file

class First {
  public static void main(String[] args){
	  System.out.println("We are in public class");
  }   
}

output:- First.class

2) Can you have the public class with different name for file and class?

No. if the class is public then you should have the same name for both class and file.

File.java
class Second {
  public static void main(String[] args){
	  System.out.println("We are in public class");
  }   
}

Above program is going to throw compile time exception.

3) Will the program execute if you skip  String args[] from main method?  

No. Java compiler wont' recognize that method as main method.
java compiler looks for this method signature

public static void main(String[] args)

4) Write sum of two numbers by taking input 
import java.util.Scanner; //V5
public class ReadInput{
  public static void main(String args[]){
  	Scanner s = new Scanner(System.in);
  	System.out.println("Enter two numbers");
  	int a = s.nextInt();
  	int b = s.nextInt();
  	int c = a+b;
  	System.out.println("Sum of two numbers: " + c);
  }
}

5) What are different methods available in Scanner class?
nextInt()
nextDouble()
nextFloat()
next()
nextLine()
nextBoolan()
nextLong()
hasNextInt()
hasNextFloat()

6) What happens if you give different input eg:Float input but you are expecting int input?

You nee to enter integer as input. but you entered float then 

We are going to get inputMistMatch Run time exception.
Program wont extecute next statement.

Exception in thread "main" java.util.InputMismatchException

7)Who is responsible for converting bytecode into machine specific code?

JVM is responsible for converting bytecode to machine specific code.

8) Understadnding java data types?
https://bnymellon.udemy.com/course/java-se-programming/learn/lecture/15683698#overview

*** 10) why compile time  languages are faster than run time languages?


The idea that compiled languages are inherently faster than interpreted or runtime languages is not entirely accurate. Both compiled and interpreted languages have their own advantages and disadvantages, and the performance differences between them can vary depending on various factors. Here's a breakdown:

Compiled Languages:

In compiled languages like C, C++, and Rust, the source code is translated into machine code (binary) by a compiler before execution. This machine code is specific to the target architecture (e.g., x86, ARM), which allows for direct execution by the CPU.
Compiled languages often offer better performance because the compiler can perform optimizations during the compilation process. These optimizations can include things like dead code elimination, loop unrolling, and register allocation, which can improve the efficiency of the resulting binary code.
Once compiled, the program generally does not require an additional translation step during execution, leading to potentially faster runtime performance.
Interpreted/Runtimes Languages:

In interpreted languages like Python, JavaScript, and Ruby, the source code is executed line-by-line by an interpreter at runtime. There's no separate compilation step, and the code is translated into machine code or intermediate bytecode instructions on-the-fly.
Interpreted languages typically have slower startup times compared to compiled languages because the interpreter needs to parse and execute the code as it encounters it. However, modern interpreters often use techniques like just-in-time (JIT) compilation to improve performance by dynamically compiling frequently executed code segments into native machine code.
Interpreted languages can offer benefits such as portability, ease of development, and dynamic typing, but they may sacrifice some performance compared to compiled languages, especially for CPU-intensive tasks.
In summary, whether a language is compiled or interpreted does not solely determine its performance characteristics. Many factors, including the quality of the compiler or interpreter, the efficiency of the generated code, and the nature of the program being executed, can influence performance. Additionally, advancements in compiler technology, runtime optimizations, and hardware capabilities continue to narrow the performance gap between compiled and interpreted languages.

11) Difference between declaration and initializaton of variables? what happens if you call just declared local variable ?

Each variable in java must have data type.

There are 2 steps in using variables
variable declaration :-
// variable declaration
byte max;

variable initialization :- 
// variable initialization
max = 100;

We can also do both steps at the same time.
// Variable declaration and initialization
byte min = -127;

During program execution we can change the value of variable.

Whic type you need to use for variable is based which value you are storing.
if you store small value (eg: 100) then you can use byte type.
if you store big value (eg: 100000) then you can use int type. 

byte mid;
// its going throw exception saying 
// error: variable mid might not have been initialized
System.out.println("mid: " + mid);


So if you call local variables with out initalizing then its going to throw error saying  "variable mid might not have been initialized"

***12) Whats the difference between single precission i.e float vs double precision i.e double?

In Java, single precision and double precision are two different data types used to represent floating-point numbers with different levels of precision. Here's an overview of each:

Single Precision (float):

In Java, the float data type is a 32-bit floating-point type.
Single precision numbers are represented using 32 bits, with 1 bit for the sign, 8 bits for the exponent, and 23 bits for the significand (also known as the mantissa).
Single precision numbers have a smaller range and precision compared to double precision numbers.
The range of values that can be represented by a float is approximately ±3.40282347 × 10^38, and it typically has around 7 decimal digits of precision.
Single precision floating-point numbers are suitable for many applications where precision is not critical or memory usage is a concern.
Double Precision (double):

In Java, the double data type is a 64-bit floating-point type.
Double precision numbers are represented using 64 bits, with 1 bit for the sign, 11 bits for the exponent, and 52 bits for the significand.
Double precision numbers have a larger range and higher precision compared to single precision numbers.
The range of values that can be represented by a double is approximately ±1.79769313486231570 × 10^308, and it typically has around 15 decimal digits of precision.
Double precision floating-point numbers are commonly used in applications that require higher accuracy, such as scientific calculations, financial computations, and graphics rendering.
In summary, the main differences between single precision and double precision in Java are the number of bits used to represent each type, their respective ranges, and the precision of the values they can store. Double precision provides higher precision and a larger range compared to single precision, but it also requires more memory to store. 

13)Can two variables have same name with different data types? 

No. two variables should not have same name even though they are different types.

int x = 10;
float x = 34;

it's wrong!

14) What the rules for declaring variables?

  1. Case Sensitive 

     // Both are different variables. 
     int amount;
     int Amount 

  2. can contain Alphabets, Numbers, _, $


  3) Starts with Alpahabets, _, $

   int $Amount=345;
   int max_price=345;
   int score=456;
   int _price=345;
   int room34;
   float total$Amount;
   int roll_number$Student;



   // invalid names
   int 1X;
   int #found;
   int rool number; // Space is not allowed

  4) Should not be a keyword

   // Which throws error.
   String float = "hello";

  5) Should not be a class name. if class is also in use.

//  its not good convention to use class names as variable names
  int String = 10; 

  float Integer=34.56;
  
  6) No limit on lenght of the name.

  int numberOfStudentsInCseDepartmentInEngineeringClg;

  7) Follow Camel Case.
  int maxScore, minPrice;

15) Any value with fraction/decimal  which type?
Any value with out fraction/decimal which type?

https://bnymellon.udemy.com/course/java-se-programming/learn/lecture/17899628#notes

value 456 -> By default this is int type
value 3.1445 -> By default this is decimal type. its not float type. if you want float type then you should declare as 3.45f;
Eg: float price = 3.45;

// below line is going to throw error why because
3.145 is double literal.
int area = 3.145 * radius * radius;

byte,short, int follows int literal
long -> l or L
float -> f or F
double -> d or D (default is double for fractions)
char -> ''
boolean -> true/false


Eg:
// its going to throw error. i.e  incompatable type. Possible loss of value. Why because 123456666666 is going to assume as int literal and it exceeded int range.so throwing error. 

long l = 234; // valid
long lo = 123456666666;  // invalid
long lo1= 123456666666l; // valid

int i = 123L; // invalid assigning long literal to int
float price1 = 1234.234; // invalid. incompatable type. Possible loss of value Assigning double to float.
float price2 = 1234.234f; //valid. Assigning double to float.

We can use _ in between the digits

long l = 999_999_999_000l;


16)Char literal vs String literal?

if you use single quotes then its char literal.
char literal should have single character.

if you use double quotes then its string literal.
string literal have multiple characters

char ch = 'x';

String name="Sundar";

17) How intiger literals can be represented?

Integer literals can be represented in various formats
such as

1) Decimal System :- Decimal system has numbers from 0 to 9

byte b0 = 23;

1) binary literals: can take only 2 values i.e 0 or 1
byte b1 = 0b1010

2)octal literals :can take values from 0 to 7 range 
byte b2 = 045

3) Hexa literals: can take values from 0 to 9 and A to F
byte b3 = 0XA;

18) Why java has 4 integral data types? what's the reason behind it?
Java has 4 integer types. They are

1)byte -> it takes 1 byte space i.e 8 bits
2)short -> it takes 2 byte space i.e 16 bits
3)int -> it takes 4 byte space i.e 32 bits
4)long -> it takes 8 byte space i.e 64 bits

Why we have 4 bytes for int ?

Current generation processors i.e CPU are of 
32 bit processor/ 64 bit processor.
i.e CPU can process 32 bits or 64 bits on one short.

older version of CPU can process less data i.e 32 bits/16 bits in one short.

let us say if 32 bits processor need to process 64 bit long type data then processor is going to process in 2 steps i.e 2 cpu cycles instead of one cpu cycle/ step like how we are summing big numbers in multiple steps.So if the capacity of processor is less than given data then it's going to take multiple steps to process the data.

When java was introduced 32 bit machines are there in the market. So therefore java was using 4 bytes for integer.

To support old machines i.e 8/16/32 bit processors java has 4 integral types and byte, short can also save memory why because they take less bits.

**19)How negative numbers are saved in computers?
In computers, negative numbers are typically represented using a method called two's complement. Two's complement is a binary representation scheme that allows both positive and negative numbers to be stored using the same binary arithmetic operations.

Here's how two's complement representation works:

Sign Bit: The leftmost bit (most significant bit) of the binary number represents the sign of the number. If this bit is 0, the number is positive; if it is 1, the number is negative.

Magnitude: The remaining bits represent the magnitude of the number using binary notation. The magnitude is the absolute value of the number.

To represent a negative number using two's complement:

Start with the binary representation of the absolute value of the number.
Invert (flip) all the bits.
Add 1 to the result.
Let's take an example with a 4-bit representation:

To represent -3:

The binary representation of 3 is 0011 (positive).
Invert the bits: 1100.
Add 1: 1101.
So, -3 is represented as 1101 in two's complement.
To represent -7:

The binary representation of 7 is 0111 (positive).
Invert the bits: 1000.
Add 1: 1001.
So, -7 is represented as 1001 in two's complement.
When performing arithmetic operations with two's complement numbers, the hardware interprets the leftmost bit as the sign bit and applies appropriate operations to handle signed arithmetic. This representation simplifies arithmetic operations and eliminates the need for separate operations for handling negative numbers.

Two's complement representation is widely used in modern computer systems because it provides a convenient way to represent signed integers while allowing for efficient arithmetic operations using standard binary arithmetic circuits.

20) Why we are using 2's complement for storing negative numbers?

https://www.youtube.com/watch?v=sJXTo3EZoxM

21) How to check binary format of a given decimal number in java?

We can use Integer.toBinaryString(5) -> 
Integer.toBinaryString(-5) -> its going to show negative number

22) Whats the result of below program?
int x=5, y=4, z;
z = 2 * x++ + 3*++x;
System.out.println(z);

At the begining x is 5 so 2*5 => 10
x got incremented to 6 because of  x++
x got incremented again because of ++x to 7
Now 2*5 + 3*7 => 21

Answer is 21

23)can we use preincrement and postincrement operators on characters?

Yes. Why because internally characters are stored as numbers. numbers are mapped to symbols.
Eg: 65 is mapped to 'A'

So now if char ch ='C' 
int x = ++ch;
So the answer is 68 why because is C is 67 + 1

**24) What's the difference between these two lines?
byte b1=5;
System.out.println(++b1);
  vs

byte b1= 5;
b1 = b1+1;
System.out.println(b1);

In the second case we are going to compile time error.
Why because all numbers without decimals are integer literals. i.e here 1 is int literal.
So you adding byte type + int literal type -> result should be int type.
But here you are adding it to int type.
That's the problem.

Not only that when you perform arithmetic operations on byte,short,int type then result should be of int type only.
byte+byte => output is int type
byte+short => output is int type
short+short => output is int type


In the first case output is 6
Why because when you performing increment/decrement on the variable type then the increment/decrement is going to perform on the same variable type.

**25) How can swap numbers without using extra number using bitwise operators?

We can use xor operation  i.e exclusive or operation to swap numbers.

how it works?

int a = 12;
int b = 9;
a = a ^ b; // it has the values for both a and b
b = a ^ b; // Now here we are removing b
a = a ^ b;

The XOR (exclusive OR) operation can be used to swap two numbers without using a third variable. This method exploits the properties of XOR, namely:

A ⊕ A = 0
A ⊕ 0 = A
XOR is commutative and associative
Here's how the swap works:

Let's say we have two variables a and b, and we want to swap their values.

a = a ⊕ b
b = a ⊕ b
a = a ⊕ b
Let's walk through this step by step:

1) a = a ⊕ b: At this point, a contains the result of the XOR operation between the original values of a and b.
2) b = a ⊕ b: Since a now holds the result of the XOR operation between the original a and b, when we XOR it with the original b, we effectively cancel out the original b and obtain the original value of a.
c) a = a ⊕ b: Now, since a still holds the result of the original a XOR b, XORing it with the new value of b (which is the original value of a) cancels out the original a and gives us the original value of b.

26) How can we use bitwise operators to mark one bit turned on / how to check one bit is on or off?
https://bnymellon.udemy.com/course/java-se-programming/learn/lecture/17927726#notes

28) What's the difference between String + and concat() method?

In Java, both String.concat() method and the + operator can be used to concatenate strings. However, there are some differences between them:

Concatenation Operator (+):
The + operator is commonly used for concatenating strings in Java.
It's easy to use and widely recognized for string concatenation.
It can be used directly between string literals, variables, or expressions involving strings.
Example:

String str1 = "Hello";
String str2 = "World";
String result = str1 + " " + str2; // "Hello World"
String.concat() Method:
String.concat() is a method defined in the String class.

It specifically concatenates the specified string to the end of the invoking string.
It can only concatenate one string at a time, so if you want to concatenate multiple strings, you need to call concat() multiple times.
Example:

String str1 = "Hello";
String str2 = "World";
String result = str1.concat(" ").concat(str2); // "Hello World"

Clarity and Readability:

The + operator is generally more readable and intuitive, especially when concatenating multiple strings and variables together.
concat() method calls may clutter the code, particularly when concatenating multiple strings.
Performance:

In most cases, there's no significant difference in performance between + and concat().
The Java compiler often optimizes + concatenation into a StringBuilder operation behind the scenes, making it efficient.
However, excessive use of + for concatenation in loops or large-scale string operations might lead to performance issues due to repeated instantiation of StringBuilder objects. In such cases, StringBuilder or StringBuffer should be used directly.
Immutability:

Strings in Java are immutable, meaning that any operation on a string generates a new string rather than modifying the existing one.
Both + and concat() follow this immutability principle. They create a new string object containing the concatenated result without modifying the original strings.

29) What is fall through in switch case?
if you wont add break statement inside case statement then it will execute next case statement and this continue to execute case statements untill it find break statement  or swith case ends.

30) can you change the order of case statements?
Yes you can keep case statements in any order.

31) Which data types are supported in case statements?

Except float, double rest are valid.

So we can give byte, short, int, char, string types.
String type support is added in java 1.7

case 1
case 'a'
case "yes"

32) Where the switch cases are most useful?
Switch cases are mostly useful in writing menu driven programs.

Eg:When you click on File -> its going to show menu
NEW
OPEN
SAVE
SAVE AS
Close

33) Switch vs else if?
in else if block it's going to verify each condition untill it find's exact match.
let us say

 if (day == 0) {
            System.out.println("Sunday");
        } else if (day == 1) {
            System.out.println("Monday");
        } else if (day == 2) {
            System.out.println("Tuesday");
        } else if (day == 3) {
            System.out.println("Wednesday");
        } else if (day == 4) {
            System.out.println("Thursday");
        } else if (day == 5) {
            System.out.println("Friday");
        } else if (day == 6) {
            System.out.println("Saturday");
        }

    if  you given day as 5 then it nee to check first 4 condition then only it can come to 5th conition block.

    But in case of switch statement it's going to called case directly. it won't execute each case until it reach called case. 


     switch (day) {
            case 1:
                System.out.println("Sunday");
                break;
            case 2:
                System.out.println("Monday");
                break;
            case 3:
                System.out.println("Tuesday");
                break;
            case 4:
                System.out.println("Wednesday");
                break;
            case 5:
                System.out.println("Thursday");
                break;
            case 6:
                System.out.println("Friday");
                break;
            case 7:
                System.out.println("Saturday");
                break;
            default:
                System.out.println("Invalid day");
        }

So Switch case is faster than if else conditions.
