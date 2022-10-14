# Arrays 

<<<<<<< HEAD
=======
An *array* is a container object that holds a fixed number of values 
of a single type. The length of an array is established **when the 
array is created**. 

After creation, an array's length **is fixed**. Each item in an array 
is called an *element*, and each element is accessed by its *numerical 
index*. 

![array](https://user-images.githubusercontent.com/109105989/195759009-8bfe18b6-b981-4f2f-aeb0-5ca71d28ce37.png)

## Declaring a variable to refer to an Array 
``` java 
// declares an array of integers
int[] anArray;
``` 

Like declarations for other Java types, an array declaration 
has two components: the **array's type** and the **array's name**. 

### Declaring arrays of different types: 
``` java 
// declaring an array of different types
byte[] anArrayOfBytes;
short[] anArrayOfShorts;
long[] anArrayOfLongs;
String[] anArrayOfStrings;
``` 

## Creating, Initializing, and Accessing Arrays 
You can create arrays with the **new** operator, followed by the amount of memory you'd like to allocate to the such array. 

### Creating an array
``` java 
// creating an array of 10 integers
int[] randomInts = new int[10];
        
// creating an array by shorthand 
int[] shorthandArray = {1, 2, 3, 4, 5}; 
``` 

### Initializing an array 
``` java 
int[] randomInts = new int[10];

randomInts[0] = 1; // initializes the first element on the array 
randomInts[1] = 2; // initializes the second element 
randomInts[2] = 3; // and the third
``` 
### Accessing an array 
``` java 
// Printing the elements 
System.out.println("Element 1 at index: " + randomInts[0]); // Prints 1 
System.out.println("Element 2 at index: " + randomInts[1]); // Prints 2 
System.out.println("Element 3 at index: " + randomInts[2]); // Prints 3
``` 

# References 
Java. (2022). *Learn Java*. <https://dev.java/learn/> 
>>>>>>> 524777de398d54608187eea4a4f3e12ea6b6ed99
