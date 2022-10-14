# Functions 

In Java, functions are first-class
types. This means, just as you can
pass numbers to methods and have methods
return numbers, you may have arguments
and return values that are functions.

Functions that process or return functions
are called higher-order functions.

## Higher-Order Functions
Map/Filter/Reduce allow us to operate
on sequences with no explicit control
flow (not a single for loop or if statement).

Higher order functions are similar to iterating
through values, but at a higher level. Higher-order
functions treat the entire sequence of elements as
a unit, so that the programmer DOESN'T HAVE TO name
and work with the elements individually.

In this paradigm control flow statements disappear.

Java has an abstract database type "Stream<E>"
that represents a sequences of elements of type
E.

Collection types like List and Set provide a
stream() method that returns a Stream for the
collection.
