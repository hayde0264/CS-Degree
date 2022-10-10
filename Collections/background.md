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
  
  CrossJoin(array ...[]interface{}) MultiDimensionalArray /* Joins the collection's values among the given arrays or collections, returning a Cartesian 							     product will all possible permutations.*/ 
  Dd()                                    // Dumps the collection's items and ends execution of the script. 
  
  Diff(interface{}) Collection            /* Compares the collection against another collection or a plain PHP array based on its values. This method 						    will return the values in the original collection that are not present in the given collection. */
  DiffAssoc(map[string]interface{}) Collection            /* Compares the collection against another collection or plain PHP array based on its values. 
                                                             This method will return the key/value pairs in the original collection that are not present 							      in the given collection.*/
  Dump()                                  // Dumps the collection's items. 
  
  Each(func(item, value interface{}) (interface{}, bool)) Collection      /* Each iterates over the items in the collection and passes each item to 										     callback. */  
  Every(CB) bool                          // Verifies elements of a collection pass a truth test. 
  
  Every(CB) bool                          // Verifies elements of a collection pass a truth test. 
  
  Except([]string) Collection             // Returns all items in the collection except for those with specified keys. 
  
  Filter(CB) Collection                   // Filters the collection using the given callback, keeping only those items that pass a given truth test. 
  
  First(...CB) interface{}                // Returns the first element in the collection that passes a given truth test. 
  
  FirstWhere(key string, values ...interface{}) map[string]interface{}    // Returns the first element in the collection with the given key/value pair. 
  
  FlatMap(func(value interface{}) interface{}) Collection                 /* Iterates through the collection and passes each value to the given 										     callback.*/  
  Flip() Collection                       // Swaps the collection's key with their corresponding values. 
  
  Forget(string) Collection               // Removes an item from the collection by its key. 
  
  ForPage(int, int) Collection            // Returns a new colleection containing items that would be present on a given page number. 
  
  Get(string ...interface{}) interface{}                  // Returns the item at a given key. If the key does not exist, null is returned. 
  
  GroupBy(string) Collection              // Groups the collection's items by a given key. 
  
  Has(...string) Bool                     // Determines if a given key exists in the collection. 
  
  Implode(string, string) string          // Joines the items in a collection. Its arguements depend on the type of items in the collection. 
  
  Intersect([]string) Collection          // Removes any values from the original collection that are not present in the given collection. 
  
  IntersectByKeys(map[string]interface{}) Collection      /* Removes any keys from the original collection that  are not present in the given 									     collection.*/ 
  isEmpty() bool                          // Returns true if the collection is empty; otherwise false is returned. 
  
  isNotEmpty() bool                       // Returns true if the collection is not empty; other false is returned. 
  
  KeyBy(interface{}) Collection           /* Keys the collection by the given key. If multiple items have the same key, only the last one will appear in 					      the new collection.*/ 
  Keys() Collection                       // Returns all of the collection's keys. 
  
  Last(..CB) interface{}                  // Returns the last element in the collection that passes a given truth test. 
  
  MapToGroups(MapCB) Collection           // Groups the collection's items by the given callback. 
  
  MapWithKeys(MapCB) Collection           // Iterates through the collection and passes each value to the given callback. 
  
  Median(...string) decimal.Decimal       // Returns the median value of a given key. 
  
  Merge(interface{}) Collection           /* Merges the given collection with the original collection. If a string key in the given items matched a 						     string key in the original collection, 
                                             the given item's value will overwrite teh value in the original collection. */
  Pad(int, interface{}) Collection        // Fills collections with the given element until the array reaches the specified size. 
  
  Partition(PartCB) (Collection, Collection)              // Seperates elements that pass a given truth test from those that do not. 
  
  Pop() interface{} Collection            // Removes and returns the last item from the collection. 
  
  Push(interface{}) Collection            // Appends an item to the end of the collection. 
  
  Random(...int) Collection               // Returns a random item from the collection. 
  
  Reduce(ReduceCB) Collection             // Reduces the collection to a single value, passing the result of each iteration into the subsequent iteration. 

  Reject(CB) Collection                   // Filters the collection using the given callback. 
  
  Reverse() Collection                    // Reverse the order of the collection's elements, preserving the original keys. 
  
  Search(interface{}) int                 /* Searches the collection for the given element and returns its key if found. If the item is not found, -1 is 					      returned. */ 
  
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
