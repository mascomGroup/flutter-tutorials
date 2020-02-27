## Welcome to dart programming

We are going to write our first program in dart programming language. To avoid wastage of time, I am not going to teach about environment setup for dart programming because we cover that stage in the previous tutorial. We are going to use dartPad to write code and compilation. Dartpad is an online tool to write and execute a dart code. Visit the following link to use the dartpad [https://dartpad.dartlang.org/](https://dartpad.dartlang.org/).

### Hello Word 

copy and paste the following code 

    void main(){
    
      print('Hello Word');
      
    }
    
 ![firstProgram_in_Dart](http://codeswag.co.uk/wp-content/uploads/2020/02/Screenshot_2020-02-24_16-22-52.v1-scaled.jpg  "hello_world")
    
 please take note, dart is case sensitive, also ignores spaces, tabs, and newlines that appear in programs. Also, each dart line of instruction must end with a semicolon (;). 
 
 Dart supports the following types of comments.
 
    

    Single-line commenting  ( // ) − Any text between a "//" and the end of a line is treated as a comment

    Multi-line comments (/* */) − These comments may span multiple lines.

##Object-Oriented Programming in Dart

Object-Oriented Programming is a software development process that follows real-world modeling.

###What is an object

An object is a real-time representation of any entity. The object consists of three features.

###1. State

Described by the attributes of an object.

###2. Behavior

Describes how the object will act.

###3. Identity 

a unique value or feature that distinguishes an object from other related objects. For example, a classroom consists of students and the student registration number will act as the identity because it is a unique value.

### Class

Class is a blueprint for creating objects

### Method

The method in object-oriented programming is used to facilitate communication between objects.

###Dart and Object Orientation

copy and paste the following code.

    class HelloWord {   
    
    // HelloWorld is the class name
    
    void method1() {     
    
    // method1 is name of the method.
    // void means that method1 is returning nothing.
     print("Hello World"); 
    } 
    }   
    void main() {   
    
    // creating object test of the class HelloWorld
    
    HelloWorld test = new HelloWord();   
    
    // calling the object
    test.method1();  
    }

  
##Data Types in Dart Programming

###1. Numbers

Numbers consist of Integer and double. Integer consists of whole numbers only and  Double consists of numeric values i.e. values with decimal points. The Double data type in Dart represents a 64-bit (double-precision) floating-point number.


###Strings

A string is a sequence of characters. String values are embedded in either single or double-quotes.


###Boolean

Dart uses the bool keyword to represent boolean values, boolean values can be either true or false.


###List and Map

These data types are used to represent a collection of objects in dart. List data type in dart is synonymous with the concept of an array in other programming languages. The Map data type represents a set of values as key-value pairs.

###Dynamic 

If the type of a variable is not explicitly specified, the variable’s type is dynamic. The dynamic keyword can also be used as a type annotation explicitly.
For example.

    void main() { 
    dynamic name = "programmer"; 
    print(name);  
    }
    
##What is a variable

A variable is a named space in the memory that stores values. In other words, it acts as a container for values in a program. Variable names are called identifiers.

A variable must be declared before it is used.  The syntax for declaring a variable is as given below −

    var name = 'Programmer';
    
###Final and Const in dart programming

The final and const keyword is used to declare constants in dart programming. When variables are declared as final or const, values can not be modified. These keywords can be used in conjunction with the variable’s data type or instead of the var keyword.

see the following examples:

The syntax for final keyword

      final amount = 50;
      
      final int  amount = 50;
      
The syntax for const keyword

      const  name = 'programmer';
      
      const string name = 'programmer';
      
copy and paste the following code when we try to modify the const and final variables.

     void main() { 
     final w = 120; 
     const v = 103; 
     v = 120; 
    }
    
    
##Conditional Statements in dart programming

Dart has two operators that let you evaluate expressions that might otherwise require if-else statements.

      if(condition){
       //Execute this part of the code if the condition is true.
       else{
      //Execute this part of the code if the condition is not true.
      }
      
##Exception handling

An exception is an error occurred at runtime because Dart runtime could not execute a statement successfully or any other thousand reasons. When an exception is thrown, there is a good chance that our program will crash. 

copy and paste the following code.

     void main() {
  
    // This statement will execute
    
    print('hello dart programming');
    var result = 100 ~/ 0;
  
    // all the following statements will not execute 
   
    print('result is $result');
   
    print('results');
    
    }
    
To save our program from crashing, we need to catch an exception. This is done using try/catch/finally block you might already be familiar with. 

copy and paste the following code.

    void main() {
  
     try{
     var result = 50 ~/ 0;
   
     print('the result is $result');
     
     } on IntegerDivisionByZeroException{
     
     print("ERROR : cant devide by 0");
     
    } on FormatException catch (e) {
      
     print("Error : the format is not correct $e");
      
    }
     catch(e){
       
       print(e);
    }
   
    finally{
     
     print('Exception Handling well implemented');
    }
    
    }
    
with the above code, no probability that the program can crush as compared with the previous code where i haven't implemented exception handling. Also, you can see in this scenario the last statement was executed. See the image below of the results of the code.

## Lists

A list is simply an ordered group of objects and dart: core library provides the List class that enables creation and manipulation of lists.

###Logical presentation of a list

    Index                      values
    
    0                            24
    1                            45
    2                            56
    3                            60

The list contains in it the values 24, 45, 56, 60

Each element in the list is identified by a unique number called the index. The index starts from zero and extends up to n-1 where n is the total number of elements in the List. The index is also referred to as the subscript.

Lists are classified into two that is fixed list and growable list

### Fixed length list

its size can not be changed during run time.  The syntax for creating a fixed-length list is as given below

####step 1 - declaring a list

    var list1 = [1,2,3,4,5,6,7,];
    
    
####step 2 - initialising a list

list1[0] = 1;
list1[1] = 2;
list1[2] = 3;
list1[3] = 4;
list1[4] = 5;

Example: creating a fixed-length list and display values contained in the list.

copy and paste the code.

      void main (){  
      
       var list1 = new List(5);
       
       list1 = [1,2,3,4,5,6,7];
      
      print(list1);
      
      // Altenatively print(list1[0]);
      // print(list1[1]);
      //print(list1([2]);
      //print(list1[3]); upto index 6
      }
      
In the following example, I am going to show how to create an empty list and add values to the list dynamically. Growable list

     void main() { 
     var list1 = new List(); 
     list1.add(12); 
     list1.add(13); 
     print(list1); 
    } 

## Maps

A Map is a dynamic collection. In other words, Maps can grow and shrink at runtime. Maps can be declared using either map literals or using map constructors.

###Declaring a Map using Map Literals

To declare a map using map literals, you need to enclose the key-value pairs within a pair of curly brackets "{ }".

    var identifier = { key1:value1, key2:value2 [,…..,key_n:value_n] }

###Declaring a Map using a Map Constructor

To declare a Map using a Map constructor, First declare the map and second, initialize the map as follows:

    var identifier = new Map();
    
    // initialize the map
    
    map_name[key] = value;
    
  
###Examples of Map literal and Map Constructor

    void main(){
    
    // Map Literal
    var myList = {'username':'joseph','password':'jtmasona@0797'};
    
    // adding values to the map on run-time
    
    myList['email'] = 'jtmasona@zimind.co.zw';
   
    print('$myList');
    
    // using map constructor
    
    var details = new Map(); 
    details['Usrname'] = 'joseph'; 
    details['Password'] = 'jtmasona@0797'; 
    print(details); 
     }
     
##Set 

The set represents a collection of objects in which each object can occur only once. The dart: core library provides the Set class to implement the same. 

Syntax

    Identifier = new Set();
    
    OR
    
    Identifier = new Set.from(Iterable);
    
    // Iterable represents a list of values to add to a Set.
    
### Example

copy and paste the following code.
    
     void main() { 
     Set numberSet = new  Set(); 
     numberSet.add(100); 
     numberSet.add(20); 
     numberSet.add(5); 
     numberSet.add(60); 
     numberSet.add(70);
     print("$numberSet");  
     
     // using Set.from to add values to the set
     
     Set set1 = new Set.from([12,13,14]); 
     
     print("$set1");  
 
    }