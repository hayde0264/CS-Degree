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
  Shift() Collection                      // Removes and returns the first item from the collection. 
  
  Shuffle() Collection                    // Randomly shuffles the items in the collection. 
  
  Slice(...int) Collection                // Returns the slice of a collection starting at the given index. 
  
  Sort() Collection                       // Sorts the collection. 
  
  SortByDesc() Collection                 // Sorts the collecion in the opposite order. 
  
  Splice(index ...int) Collection         // Removes and returns a slice of elements starting at the specified index. 
  
  Split(int) Collection                   // Breaks a collection into the given number of groups. 
  
  Unique() Collection                     // Returns all of the unique items in the collection. 
  
  WhereIn(string, []interface{}) Collection               // Filters the collection by a given key/value contained within the given collection. 
  
  WhereNotIt(string, []interface{}) Collection            // Filters the collection by a given key/value not contained within the given array. 
  
  ToJson() string                         // Converts the collection into a json string. 
  
  ToNumberArray() []decimal.Decimal       // Converts the collection into a plain golang slice which contains decimal.Decimal. 
  
  ToIntArray() []int                      // Converts the collection into a plain golang slice which contains int. 
  
  ToInt64Array() []int64                  // Converts the collection into a plain golang slice which contains int64. 
  
  ToStringArray() []string                // Converts the collection into a plain golang slice which contains string. 
  
  ToMultiDimensionalArray() [][]interface{}               // Converts the collection into a multi-dimensional array. 
  
  ToMap() map[string]interface{}          // Converts the collection into a plain golang map. 
  
  ToMapArray() []map[string]interface{}   // Converts the collection into a plain golang slice with contains map. 
  
  Where(key string, values ...interface{}) Collection     // Filters the collection by a given key/value pair. 
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
