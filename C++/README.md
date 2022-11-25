# C++

# Prefer <iosstream> to <studio.h> 
  ## Why? 
  

# Prefer C++ style comments 
  
# Use delete on pointer members 
  
# Adhere to convention when writing operator new and operator delete 
  
# Write operator delete if you write operator new 
  
# Prefer initialization to assignment in constructors 
  
# Make destructors virtual in base classes 
  
# Assign to all data members using operator (=)
  
# Strive for class interfaces that are complete and minimal 
  
# Avoid data members in the public interface 
  
# Prefer pass-by-reference to pass-by-value 
  
# Choose carefully between function overloading and parameter defaulting 
  
# Guard against potential ambiguity 
  
# Partition the global namespace 
  
# Avoid member functions that return non-const pointers or references to members less accessible than themselves 
  
# Postpone variable definitions as long as possible
  
# Minimize compilation dependencies between files 
  
# Differentiate between the inheritance of interface and inheritance of implementation 
  
# Never redefine an inherited default parameter value 
  
# Model "has-a" or "is-implemented-in-terms-of" through layering 
  
# Use private inheritance judiciously 
  
# Say what you mean; understand what you say 
  
# Prefer compile-time and link-time errors to runtime errors 
  
# Pay attention to compiler warnings
  
# Improve your understanding of C++ 
  
# Prefer const and inline to #define 
  
# Prefer new and delete to malloc and free 
  
# Use the same form in corresponding uses of new and delete 
  
# Be prepared for out-of-memory conditions 
  
# Avoid hiding the "normal" form of new 
  
# Declare a copy constructor and an assignment operator for classes with dynamically allocated memory 
  
# List members in an initialization list in the order in which they are declared 
  
# Have operator (=) return a reference to (*this) 
  
# Check for assignment to self with the operator (=) 
  
# Differentiate among member functions, non-member functions, and friend functions 
  
# use const whenever possible 
  
# Don't try to return a reference when you must return an object 
  
# Avoid overloading on a pointer and numerical type 
  
# Explicitly disallow the use of implicity-generated member functions you don't want 
  
# Avoid returning "handles" to internal data 
  
# Use inlining judiciously 
  
# Make sure public inheritance models "is-a" 
  
# Never redefine an inherited nonvirtual function 
  
# Avoid casting down the inheritance hierarchy 
  
# Differentiate between inheritance and templates 
  
# Use multiple inheritances judiciously 
  
# Know what functions C++ silently writes and calls 
  
# Ensure that non-local static objects are initialized before they're used 
  
# Familiarize yourself with the standard library 
  
# References 
Meyers, S. (1997, January 1). *Effecitve C++* (2nd ed.). Addison Wesley. <https://www.amazon.com/Effective-Specific-Addison-Wesley-Professional-Computing/dp/0201924889/ref=sr_1_8?crid=2E3FNEKRSDV3I&keywords=effective+c%2B%2B&qid=1669348261&sprefix=effective+c%2B%2B+%2Caps%2C68&sr=8-8>
