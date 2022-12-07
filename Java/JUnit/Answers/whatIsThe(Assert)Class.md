# What is the Assert class? 


**Assert class** - provides methods for checking values and reporting errors 


## Methods included: 
```java 
void assertTrue(boolean) // reports an error if the boolean is false 
void assertTrue(String, boolean) // reports an error identified by String if the boolean is false 
void assertFalse(boolean) // reports an error if the boolean is true 
void assertNull(Object) // reports an error if the Object is not null 
void assertNull(String, Object) // reports an error if Object is null 
void notNotNull(Object) // reports an error if the Object is null 
void assertNonNull(String, Object) // reports an error identified by String if Object is null 
void assertSame(String, Object, Object) //report an error identified by String if the two Objects are not identical 
void assertNotSame(Object, Object) // reports an error if two Objects are identical 
void assertNotSame(String, Object, Object) //report an error identified by String if two Objects are identical 
void assertEquals(String, Object, Object) //report an error identified by a String if two Objects are not equal 
void assertEquals(String, String) // reports an error if two Strings are not equal. Error reported as the delta between two Strings 
void assertEquals(boolean, boolean) // reports an error if two booleans are not equal 
void assertEquals(String, boolean, boolean) //report an error identified by String if two booleans are not equal 
void assertEquals(byte, byte) // reports an error if the two bytes are not equals 
void assertEquals(String, byte, byte) //report an error identified by a String if two characters are not equal 
void assertEquals(char, char) // reports an error if two chars are not equal 
void assertEquals(String, char, char) //report an error identified by String if two cars are not equal 
void assertEquals(short, short) // reports an error if two shorts are not equal 
void assertEquals(String, short, short) //report an error identified by String if two shorts are not equal
void assertEquals(int, int) // reports an error if two ints are not equal 
void assertEquals(String, int, int) //report an error identified by String if two ints are not equal 
void assertEquals(long, long) // reports an error if two longs are not equal 
void assertEquals(String, long, long) //report an error identified by String if two longs are not equal 
void assertEquals(float, float, float) // reports an error if the first two floats are not within epsilon of each other 
void assertEquals(String, float, float, float) //report an error identified by String if the first two floats are not within epsilon of each other 
void assertEquals(double, double, double) // reports an error if the first two doubles are not within epsilon of each other 
void assertEquals(String, double, double, double) //report an error identified by String if the first two doubles are not within epsilon of each other 
void fail() // reports an error 
void fail(String) // reports an error identified by String 
``` 

# References 
Beck, K. (2003, September 23). *JUnit Pocket Guide*. O'Reilly Media. <https://www.amazon.com/JUnit-Pocket-Guide-Look-up-Advice-ebook/dp/B002QX43Z2/ref=sr_1_15?crid=2CZMB5XJF1GXM&keywords=junit&qid=1670452993&sprefix=junit+%2Caps%2C83&sr=8-15>w 
