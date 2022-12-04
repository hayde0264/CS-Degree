# Count occurances 

**time** - O(n) 


## In Java: 
```java
  
  public class Test {
  
          public static int countOccurances(int arr[], int key) {
                  int count = 0;
                  for (int i = 0; i < arr.length - 1; i++) {
                          if (arr[i] == key) {
                                  count++;
                          }
                  }
                  return count;
          }
  
  
          public static void main(String[] args) {
                  int arr[] = {1, 2, 2, 2, 3, 4};
                  int key = 2;
                  int test = countOccurances(arr, key);
  
                  String ouput = arr.length != 0 ? "Element " + key + " occurs " + test + " times." : "Element doesn't exsist within collection";
  
                  System.out.println(ouput); // Prints - Element 2 occurs 3 times.
          }
  }
``` 

