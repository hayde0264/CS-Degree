# Binary Search 

Problem - given a shorted array of (x) integers and a key value, 
	  determine if the key exsist in the array in logarithmic 
          time. If the key exsists, print the index of it. 

*Binary search* is a divide-and-conquer algorithm. Like all divide-
and-conquer alroithms, binary search first divides an array into 
two small subarrays, then it discards one subarray and continues on
the second subarray. This decision of "discarding" one subarray is 
made in only ONE comparision. 

## What makes Binary Search Impressive? 
Binary search reduces the search space to half at each step. By 
spare space, we mean a subarray of the given array where the key 
value is located (if present within the array). Initially, the search 
space is the entire array, but binary search reduces the space at each
of the algorithm by using the property of the array that it is sorted. 


## How does the algorithm operate? 
Binary search compares the mid-value in the search space to the key value. 
If the key value matches the middle element, its position in the array is 
returned; otherwise, it discards half of the search space based on the 
comparison result. 

### Psedocode 
1. if key = array[middle], return middle
2. if key < array[middle], discard elements in right search space & the middle element 
3. if key > nums[middle], discard elements in the left search space & the middle element 

# References 
TECHIE DELIGHT. (n.d.) *Binary Search Algorithm - Iterative and Recursive Implementation*. 
	<https://www.techiedelight.com/binary-search/>
