# Collections 

In programming, a *collection* is a class 
that's used to represent a group of similar 
data as a **single type**. 

Collections **group** and **manage** related objects. 

## What's the point of collections? 
Collections use their underlying data structure 
to **store** and **manipulate** data effectively. 

## Most modern languages break collections into: 
*Lists* - also known as arrays, lists are collections 
          that except duplicate elements and are 
	  accessible through indexing the elements 
          within the list.
 
*Sets* - are collections that **do not** allow 
	 duplicate elements.
 
*Maps* - also known as dictionaries, are collections 
	 that contain key/value pairs. Maps **cannot** 
	 contain duplicate pairs. 

### You may perform the following operations on collections:  
- Searching 
- Deletion 
- Insertion 
- Traversal 
- Sorting 
- Cloning 

## Java Collection Heirachy 
``` java 

``` 
## Go Collection Heirachy 
``` go 
Last login: Sun Oct  9 19:53:35 on ttys000
haydenhowell@Haydens-Mac-mini ~ % vim collections.go 






















  
>>All() []interface{} // Returns the underlying array represented by the collection. 
  
  Length() int        // Returns the length of the collection.
  
  ToStruct(dist interface{})              // Turns collections into specified structs using mapstructure. 
  
  Select(keys ...string) Collection       // Select the keys of collections and delete others. 
  
  Avg(key ...string) decimal.Decimal      // Returns the average value of a given key. 
  
  Sum(key ...string) decimal.Decimal      // Returns the sum of all items within a collection. 
  
  Min(key ...string) decimal.Decimal      // Returns the minimum value within a collection. 
  
  Max(key ...string) decimal.Decimal      // Returns the maximum value within a collection. 
  
  Join(delimiter string) string           // Returns a string of joined values. 
  
  Count() int                             // Returns the total number of items within a collection.
  
  Pluck(key string) Collection            // Retruns specified values within a collection. 
  
  Mode(key ...string) []interface{}       // Returns the mode value of an element. 
  
  Only(key []string) Collection           // Returns the collection with only specified elements. 
  
  Prepend(values ...interface{}) Collection       // Adds an item to the beginning of a collection. 
  
  Pull(key interface{}) Collection                // Removes and returns an element from the collection. 
  
  Put(key string, value interface{}) Collection   // Sets the given key and value within a collection. 
  
  SortBy(key string) Collection           // Sorts the collection by the given key. 
  
  Take(num int) Collection                // Returns a new collection with a specified number of elements. 
  
  Chunk(num int) MultiDimensionalArrayCollection          // Breaks the collecetion into multiple, smaller collection of a given size. 
  
  Collapse() Collection                   // Collapses a collection of arrays into a single-flat collection. 
  
  Concat(value interface{}) Collection    // Appends the given array or collection values onto the end of the collection. 
  
  Contains(value ...interface{}) bool     // Determines whether the collecetion contains a given element. 
  
  CountBy(callback ...interface{{) map[interface{}] int   // Counts the occurances of values in the collection. By default, the method counts the occurences of each element. 
  
  CrossJoin(array ...[]interface{}) MultiDimensionalArray // Joins the collection's values among the given arrays or collections, returning a Cartesian product will all possible permutations. 
  
  Dd()                                    // Dumps the collection's items and ends execution of the script. 
  
  Diff(interface{}) Collection            /* Compares teh collection against another collection or a plain PHP array based on its values. This method will return the values in the original col                                            lection that are not present in the given collection. */
  DiffAssoc(map[string]interface{}) Collection            /* Compares the collection against another collection or plain PHP array based on its values. 
                                                             This method will return the key/value pairs in the original collection that are not present in the given collection.*/
  Dump()                                  // Dumps the collection's items. 
  
  Each(func(item, value interface{}) (interface{}, bool)) Collection      // Each iterates over the items in the collection and passes each item to callback. 
  
  Every(CB) bool                          // Verifies elements of a collection pass a truth test. 

``` 
## Swift Collection Heirachy 
``` swift 
// MARK: Acessing A Collections's Elementts
subscript(Self.Index) -> Self.Element        // Accesses the element at the specified position.

// MARK: Selecting and Excluding Elements
func popFirst() -> Self.Element             // Removes and returns the first element of the collection.
func removeFirst() -> Self.Element          // Removes and returns the first element of the collection.
func removeFirst(Int)                       // Rmoves the specified number of elements from the beginning of the collection.

// MARK: Manipulating Indices
var startIndex: Self.Index                  // The position of the first element in a nonempty collection
var endIndex: Self.Index                    // The collection's "past the end" position- that is, the position one greater than the last valid subscript arguement
var indices: Self.Indices                   // The indices that are valid for subscripting the collection, in ascending order
func index(after: Self.Element) -> Self.Index           // Returns the psotion immediately after the given index.
func formIndex(inout Self.Index, offsetBy: Int)         // Offsets the given index by the specified distance

// MARK: Iterating Over a Collection's Elements
func makeIterator() -> Self.Iterator            // Returns a iterator over the elements of the collection.

// MARK: Associated Types
associatedtype Element
associatedtype Index: Comparable                // A type that represents a position in a collection.
associatedtype Indices: Collection = DefaultIndices<Self>       // A type that represents the inddices that are valid for
                                                                // subscripting a collection, in ascending order.
associatedtype Iterator = IndexingIterator<Self>                /* A type that provides the collection's iteration interface
                                                                 and encapsulates its iteration state.
                                                                 */
associatedtype SubSequence:  Collection = Slice<Index>          /* A collection represeneting a contiguous subrange of this
                                                                 collection's elements. The subsequence shared indices with the
                                                                 original collection.
                                                                 */
// MARK: Instance Properties
var count: Int              // The number of elements in the collection.
var first: Self.Element?    // The first element of the collection.
var isEmpty: Bool           // A Boolean value indicating wheather the collection is empty.

``` 
## Kotlin Collection Heirachy 
``` kotlin 

``` 

# References 
*Collections*. (n.d.). <https://www.andrew.cmu.edu/course/15-121/lectures/Collections/collections.html> 

techopedia. (2022). *What Does Collection Mean?*. <https://www.techopedia.com/definition/25317/collection> 
