# C Sharp Basics


### What is C Sharp?

- C# is a general purpose language used primarily to build applications for the Windows operating system, but can be used for other purposes as well.
- For C# code to run, it first gets compiled into an intermediate language which then gets compiled into a binary that can be executed.
- Once it is an executable or '.exe' file, it can be ran immediately.
- However, C# is a language that takes advantage of a JIT compiler or Just In Time Compilation. This allows for the C# code (represented in its intermdiate language equivalent) to be compiled and executed upon the necessity for said code. This is NOT the same as above where the entire code base is compiled before execution begins.


### Additional Info

- Everything created in C# is a class that has a Main() method which gets executed upon invoking that class. Therefore, most programs will start with the following:

```
public class nameOfClass{
	
		static void Main(String[] args){


		}

}
```


### Basic Syntactical Goodness

##### Declaring Variables

```
int x = 10;

string str = "Some String";

string[] stringList = {"String1", "String2", "String3"};

int[] integerList = {1,2,3,4,5};

Dictionary<string, int> dict = new Dictionary<string,int>();

```
- C# is a strongly typed language meaning that all variable must be stated with their corresponding data type. Unlike Python, Perl, or other languages which interpret based on other factors.
- In this case, the dictionary (or key/value pair object) requires the user to specify both the data type of the keys and the data type of the values.


##### For Loop

```
for (int i =1; i<=10; i++){
	
	Console.WriteLine("This is the {0} time I have done this.", i);

};

```

- In the paretheses following the "for" statement, the order is as follows:
	- First is the variable that will be incrementing and/or decrementing.
	- Second is the range of the loop. i.e. what condition will need to be met to know the looping stops.
	- Third is the step of the for loop. In this case, it is incrementing by 1.


##### Converting Data Types

###### Type Casting

```
byte i = 1;
int x = i;

```
- The following allows for "i" to become an integer because there is no data lost, meaning the amount space required for a byte is far less than a integer and therfore is possible to be converted.

```
// SNIPPET ONE
int i = 1;
byte x = i;

// SNIPPET TWO

int i = 1;
byte x = (byte)i;
``` 
- Snippet One above will throw an error due to the byte structure/object not having the correct amout of space. 
- Therfore, in Snippet Two, we can explcitly state that we want the conversion to happen as we are stating to the compiler that it is okay for any data loss that may occur. 

###### Using Convert Library

- A common example will be converting a string represntation of a number and converting it into a integer datatype.

```
string number = "1";

int numberInt = Convert.ToInt32(number);


```

- There is a namespace in C# that allows for the use to convert various data types into numbers. In this case, we are turning a string into a number.
