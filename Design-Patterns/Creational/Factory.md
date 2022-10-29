

# Factory Design Pattern 

The factory pattern allows objects to initiate other objects **without knowing a
bout the class of the object created**. 

## The Good 
- classes initiate the creation of objects without having dependencies on the class
s of the created object 
- The set of classes a class may be expected to instantiate may be dynamic as new classes become available 


## The Bad 
- the indirection between the initiation of object creation and the determination of which class to instantiate can make it more difficult for maintenance programmers to understand 

# References
Grand, M. (2002). *Patterns in Java: A Catalog of Reusable Design Patterns Illustrated with UML, 2nd Edition, Volume 1*. Wiley. <https://www.amazon.com/Patterns-Java-Catalog-Reusable-Illustrated/dp/0471227293> 
