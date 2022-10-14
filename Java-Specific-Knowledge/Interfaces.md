# Interfaces 

There are a number of situations in software
engineering when it is important for disparate
groups of programmers to agree to a "contract"
that explains how certain software interacts.

Each group should be able to write their code without
any knowledge of how the other group's code is written.
Generally speaking, INTERFACES are such contracts.

In the Java programming language, an INTERFACE is
a reference type, similar to a class, that can contain
ONLY constants, method signatirues, default methods, static
methods, and nested types. Method bodies exsist only for
default methods and static methods.

Interfaces can not be instantiated- they can only be
implemented by classes or extended by other interfaces.

## Designing Interfaces 
1. an interface declaration consists of modifiers,
   the keyword interface, the interface name, a
   comma seperated list of parent interfaces (if
   any), and the interface body.
2. if you want your interface to be implemented
   use the public access keyword. This makes the
   interface available to any class in any package.
3. interface bodies contain abstract methods, default
   methods, and static methods. 
