Which methods do Strings support? 


## String methods include: 
- **charAt()** - retrieves a particular character in a string 
```java 
                  String a = "hayden";
  
                  char test = s.charAt(3);
                  System.out.println(test);
                  // Prints - d 
``` 
- **compareTo()** - compares a string to another string
```java 
                  String a = "hayden";
                  String b = "hayde";
  
                  int test = a.compareTo(b);
                  System.out.println(test);
                  // Prints - 0 (false) 
 ``` 

- **concat()** - concatenates a string with another string 
```java 
                  String a = "hayden";
                  String b = " howell";
  
                  String test = a.concat(b);
                  System.out.println(test);
                  // Prints - hayden howell
``` 

- **contains()** - checks whether the string contains another string 
```java 
                  String a = "hayden";
  
                  boolean test = a.contains("den");
                  System.out.println(test);
                  // Prints - true 
 ``` 
 
- **copyValueOf()** - returns a string equivalent to the specified character array  
```java 
                String a = "hayden";
                char b[] = {'a', 'b', 'c'};
  
  
                String test = a.copyValueOf(b);
                System.out.println(test);
                // Prints - abc  
```          

- **endsWith()** - checks whether the string ends with a specified suffix 
```java 
                  String a = "hayden";
  
                  boolean test = a.endsWith("ay");
                  System.out.println(test);
                  // Prints - false 
 ``` 
 
- **equals()** - compares a string to another string 
```java 
                  String a = "hayden";
                  String b = "hayden";
  
                  boolean test = a.equals(b);
                  System.out.println(test);
                  // Prints - true  
``` 

- **equalsIgnoreCase()** - compares a string with another string; ignoring the case 
```java 
                  String a = "hayden";
                  String b = "HaYden";
  
                  boolean test = a.equalsIgnoreCase(b);
                  System.out.println(test);
                  // Prints - true
``` 

- **getBytes()** - copies characters from a string into a byte array 
``` 
                  String a = "hayden";
  
                  byte[] test = a.getBytes();
                  System.out.println(test);
                  // Prints - [B@7e0e6aa2 
``` 

- **hashCode()** - returns a hashcode for a string 
```java 
          String a = "hayden";
  
          int test = a.hashCode();
          System.out.println(test);
          // Prints - -1224250003 
``` 

- **indexOf()** - searches for the first occurrence of a character or substring in a string 
```java 
          String a = "hayden";
  
          int test = a.indexOf('h');
          System.out.println(test);
          // Prints - 0 
``` 

- **intern()** - fetches a unique instance of the string from a global shared-string pool 
- **isEmpty()** - returns true if the string is empty 
- **lastIndexOf()** - searches for the last occurrence of a character or substring in a string 
- **length()** - returns the length of a string 
- **matches()** - determines if the whole string matches a regular expression pattern 
- **regionMatches()** - checks whether a region of the string matches the specified region of another string 
- **replace()** - replaces all occurrences of a regular expression pattern with a pattern 
- **replaceAll()** - replaces all occurrences of a regular expression pattern with a pattern 
- **replaceFirst()** - replaces the first occurrence of a regular expression pattern with a pattern 
- **split()** - splits the string into an array of strings using a regular expression pattern as a delimiter 
- **startsWith(()** - checks whether the string starts with a specified prefix 
- **substring()** - returns a substring from the string 
- **toCharArray()** - returns the array of characters from the string 
- **toLowerCase()** - converts the string to lowercase 
- **toString()** - returns the string value of an object 
- **toUpperCase()** - converts the string to uppercase 
- **trim()** - removes leading and trailing whitespace from the string 
- **(valueOf()** - returns a string representation of a value 




# References 
Leuck, D. & Niemeyer, P. (2013, July 16). *Learning Java: A Bestselling Hands-On Java Tutorial* (4th ed.). <https://www.amazon.com/Learning-Java-Bestselling-Hands-Tutorial/dp/1449319246/ref=sr_1_4?crid=2QA12UYY9G48E&keywords=learning+java&qid=1669249275&sprefix=learning+java+%2Caps%2C85&sr=8-4> 


