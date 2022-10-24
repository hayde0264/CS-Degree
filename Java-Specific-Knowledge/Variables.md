# Variables 

Objects store their state(s) in **fields** (a.k.a. variables). 

## Types of variables in Java: 
- Instance Variables (Non-Static Fields) 
- Class Variables (Static Fields) 
- Local Variables 
- Parameters 

# Instance Variables 
Technically speaking, object store their individual states in **"non-static fields"**, that is, fields declared **without the static keyword**. 

Non-static fields are also known as **instance variables** because their values are **unique to each instance of a class**. 

For instance the **currentSpeeed** of one **Car** is **independent** from the **currentSpeed** of another. 

## Example: 
``` Java 
// non-static instance variables
private String aString;
private Boolean aBoolean;
private int x, y, z;
``` 

# Class Variables 
A class variable is a field **declared with the static modifier**; this tells the compiler that there is **exactly one copy of this variable in existence**, regardless of how many times the class has been instantiated. 

A field defining the number of gears for a bicycle could be marked as **static since, conceptually, the same number of gears will apply to all instances**. Additionally, the keyword **final could be added to indicate that the number of gears will never change**. 

## Example: 
``` Java 
// static instance variables
static int bikeGear = 6;
static final String COMPANY_NAME  = "Oracle";
``` 

# Local Variables 
Similar to how an object stores its state in fields, a method will often **store its state in local variables**. 

The syntax for declaring a local variable is similar to declaring a field. **There is no special keyword designating a variable as local**; that determination comes entirely from the location in which the variable is declared - **which is between the opening and the closing braces of a method**. 

This means local variables **are only visible to the methods in which they're declared**; they're **not** accessible from the rest of the class. 

## Example: 
``` Java 
public void localVariables() {
    int count = 0;
    boolean isTrue = false;
    byte b = 1;
    long l = 2; 
}
```


# Paramters 
Recall that the signature for the main method is **public static void main(String[] args)**. 

Here, the **args** variable is the **parameter to this method**. 

The important thing to remember is that **parameters are always classified as "variables," not "fields"**. This applies to other parameter-accepting constructs (such as constructors and exception handlers)

``` Java 
// parameters in constructor 
Variables(String aString, Boolean aBoolean, int x, int y, int z) {
    aString = "";
    aBoolean = false;
    x = 0;
    y = 1;
    z = 2;
}
``` 

# Naming Variables
Every programming language has its own set of rules and conventions for the kinds of names that you're allowed to use, and the Java programming language is no different. The rules and conventions for naming your variables can be summarized as follows: 

## Variable names are case-sensitive: 
A variable's name can be any legal identifier - an unlimited-length sequence of Unicode letters and digits beginning with a letter, the dollar sign "$," or the underscore character. 

**The convention, however, is to always begin your variable(s) names with a letter, not the dollar sign or underscore**. 

You may find some situations where auto-generated names will contain the dollar sign, **but your variable names should always avoid using it**. 

A similar convention exists for the underscore character; while it's technically legal to begin your variable's name with the underscore, **this practice is discouraged**. 

White space is **not** permitted. 

## Subsequence characters may be: 
Letters, digits, dollar signs, or underscore characters. Conventions apply to this rule as well. 

When choosing a name for your variables, **use full words instead of cryptic abbreviations**. Doing so will make your code easier to read and understand. 

In many cases, **it will also make your code self-documenting**; fields named cadence, speed, and gear, for example, **are much more intuitive than abbreviated versions, such as s, c, and g**. 

Remember that the name you choose **must not be a keyword or reserved word**. 

## Casing 
If the name you choose consists of only one word, **spell that word in all lowercase letters**. 

If it consists of more than one word, **capitalize the first letter of each subsequent word** (ex. cityName, isUnique, CreditCardNumber). 


If your variable stores a constant value, **capitalize every letter and separate subsequent words with the underscore character**. By convention, **the underscore character is never used elsewhere**. 





# References 
Creating Variables and Naming Them. (2021, September 23).  
 
