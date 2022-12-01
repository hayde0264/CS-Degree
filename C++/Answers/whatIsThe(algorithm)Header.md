# What is the algorithm header? 

The algorithm header **(<algorithm>)** defines a collection of functions designed to be used on 
ranges of elements. 
# What is the algorithm header? 

The algorithm header **(<algorithm>)** defines a collection of functions designed to be used on sequences. 
  
## Non-Modifying sequence operations: 
- **all_of** - test condition on all elements within a range 
- **any_of** - tests if any element in range fulfills a condition 
- **none_of** - tests if no element fulfills a condition 
- **find** - finds a value within a range 
- **find_if** - finds element in range  
- **find_if_not** - finds element is range (negative condition) 
- **find_end** - finds the last subsequence in a range 
- **find_first_of** - finds an element from the set in a range 
- **adjacent_find** - finds equal adjacent elements in a range 
- **count** - counts appearances of a value within a range 
- **count_if** - returns the number of elements in a range satisfying a condition 
- **mismatch** - returns the first position where two ranges differ 
- **equal** - tets whether the elements in two ranges are equal 
- **is_permutation** - test whether a range is a permutation of another 
- **search** - searches range for subsequence 
- **search_n** - searches range for elements 
  
## Modifying sequence operations: 
- **copy** - copies range of elements 
- **copy_n** - copy element 
- **copy_if** - copy certain elements of a range 
- **copy_backward** - copies range of elements backward 
- **move** - moves range of elements 
- **move_backward** - moves a range of elements backward 
- **swap** - exchanges the values of two objects 
- **swap_ranges** - exchanges the values of two ranges 
- **iter_swap** - exchanges the values of objects pointed to by two iterators 
- **transform** - transforms a range 
- **replace** - replaces a value within a range 
- **replace_if** - replaces values in a range (conditional) 
- **replace_copy** - copies range replacing value 
- **replace_copy_if** - copies range replacing value (conditional) 
- **fill** - fills a range with a value 
- **fill_n** - fills a range with a sequence of values 
- **generate** - generates values for a range 
- **generate_n** - generates 
- **remove** - removes value from a range 
- **remove_if** - removes value from range (conditionally) 
- **remove_copy** - copies range removing value 
- **remove_copy_if** - copies a range and removes values (conditionally) 
- **unique** - removes consecutive duplicates in a range 
- **unique_copy** - copies a range and removes duplicates 
- **reverse** - reverses a range 
- **reverse_copy** - copies a reversed range 
- **rotate** - rotates left the elements within the range 
- **rotate_copy** - copies range rotated left 
- **random_shuffle** - randomly rearranges elements in range using a generator 
  
## Partitions: 
- **is_parititoned** - tests whether a range is partitioned 
- **partition** - partitions range in two 
- **stable_parititon** - partitions range into two (stably) 
- **partition_copy** - copies partition range of two 
- **partition_point** - gets partition point 
  
## Sorts: 
- **sort** - sorts elements within a range 
- **stable_sort** - sorts elements preserving the order of equivalents 
- **partial_sort** - partially sorted elements within a range 
- **partial_sort_copy** - copies and partially sorts range 
- **is_sorted** - checks whether a range is sorted 
- **is_sorted_until** - finds the first unsorted element within a range 
- **nth_element** - sorts element within range 
  
## Binary search: 
- **lower_bound** - returns an iterator to lower bound 
- **upper_bound** - returns an iterator to upper bound 
- **equal_range** - get subranges of equal elements 
- **binary_search** - tests if values exist in a sorted sequence 
  
## Merge: 
- **merge** - merges sorted ranges 
- **inplace_merge** - merges consecutive sorted ranges 
- **includes** - tests whether a sorted range includes another sorted range 
- **set_union** - sets a union of two sorted ranges 
- **set_intersection** - sets an intersection of two sorted ranges 
- **set_difference** - sets different of two sorted ranges 
- **set_symetric_difference** - sets symmetric difference of two sorted ranges 
  
## Heap: 
- **push_heap** - pushes element into heap range 
- **pop_heap** - pops an element from the heap range 
- **make_heap** - makes heap from range
- **sort_heap** - sorts elements of a heap 
- **is_heap** - tests if a range is a heap 
- **is_heap_until** finds the first element not in the heap order 
  
## Min/max: 
- **min** - returns the smallest element 
- **max** - returns the largest element 
- **minmax** returns the smallest and largest elements 
- **min_element** - returns the smallest element within a range 
- **max_element** - returns the largest element within a range 
- **minmax_element** - returns the smallest and largest element within a range 
  
## Other: 
- **lexicographical_compare** - lexicographical less-than comparison 
- **next_permutation** - transform range to next permutation 
- **prev_permutation** -- transforms range to the previous permutation 
  
## 
  
 ![c++algo](https://user-images.githubusercontent.com/109105989/204962857-41631940-92b5-46e2-bc91-ee41c9c23e6f.png)


# References 
Reference. (2022). *cplusplus*. <https://cplusplus.com/reference> 

  

