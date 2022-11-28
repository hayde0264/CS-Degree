# Which methods does List support? 

## List supports: 
```java 
  import java.util.Collection;
  import java.util.Comparator;
  import java.util.Iterator;
  import java.util.ListIterator;
  import java.util.Spliterator;
  import java.util.function.UnaryOperator;
  
  public interface List<E> {
          public boolean add(E e); // appends specified element to end of list 
          public void add(int index, E element); // inserts specified element at specified position
          public boolean addAll(Collection<? extends E> c); // appends all elements of a specified collection to the end of a list 
          public boolean addAll(int index, Collection<? extends E> c); // inserts all of the elements of a specified collection into a list at a specified position
          public void clear(); // removes all elements from a list 
          public boolean contains(Object o); // returns true if the list contains the specified element 
          public boolean containsAll(Collection<?> c); // returns true if the List contains all of the elements of a specified collection 
          public boolean equals(Object o); // compares a specified object with a list for equality 
          public E get(int index); // returns the element at a specified position in the List 
          public int hashCode(); // returns the hash code value for a list 
          public int indexOf(Object o); // returns the index of the first occurrence of a specified element in a list, or -1 if the List does not contain element 
          public boolean isEmpty(); // returns true if list contains no elements 
          public Iterator<E> iterator(); // returns an iterator over the elements within a list in proper sequence
          public int lastIndexOf(Object o); // returns the index of the last occurrence of a specified value, or -1 if the element does not exist within the List 
          public ListIterator<E> listIterator(); // returns a list iterator over the elements within a list 
          public ListIterator<E> listIterator(int index); // returns a list iterator over the elements in a list, starting at a specified position 
          public E remove(int index); // removes as element at a specified position in the List
          public boolean remove(Object o); // removes the first occurrence of a specified element from an list (if its present)
          public boolean removeAll(Collection<?> c); // removes from List all elements that are contained in a specified collection 
          public void replaceAll(UnaryOperator<E> operator); // replaces each element of a list with the result of applying the operator to that element 
          public boolean retainAll(Collection<?> c); // returns only the elements in the List that are contained in a specified collection 
          public E set(int index, E element); // replaces the element at a specified position in the List with the specified element 
          public int size(); // returns the number of elements within a list 
          public void sort(Comparator<? super E> c); // sorts the List according to the order induced by the specified Comparator
          public Spliterator<E> splitIterator(); // creates a Splititerator over the elements in a list 
          public List <E> subList(int fromIndex, int toIndex); // returns a view of the portion of a list between a specified fromIndex (inclusive) to a toIndex(exclusive)
          public Object[] toArray(); // returns an array containing all of the elements within a list in proper sequence 
          public <T>T[] toArray(T[] a); // returns an array containing all of the elements in proper sequence 
  }
``` 

## Sub and Super Classes: 
![list](https://user-images.githubusercontent.com/109105989/204170243-a60857e3-e4a6-4045-b98a-51aa91638220.png)


  
# References 
Aziz, A. Lee, T. Prakash, A. (2015). *Elements of Programming Interviews in Java* (1st ed.). <https://www.amazon.com/Elements-Programming-Interviews-Questions-Tsung-Hsien/dp/B00C7F0V3W/ref=sr_1_1?crid=SU7GU68QNL5N&keywords=elements+of+programming+interviews+in+java+1st+edition&qid=1669594847&sprefix=elements+of+programming+interviews+in+java+1st+edition+%2Caps%2C72&sr=8-1> 
