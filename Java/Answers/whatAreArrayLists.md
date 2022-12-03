# What are Array Lists? 

Array lists, which unlike arrays, are **automatically resizable** which means they don't require a **specified size**. 

The common methods in ArrayLists (size, isEmpty, get, set, iterator, and list iterator) are run in **constant time**, the add 
operation runs in **amortized constant time** O(n), and thr rest of the operations run in **linear time**. 

# Extends:
- **AbstractList<E>**

# Implements: 
- **Serializable**
- **Clonable**
- **Iterable<E>**
- **Collection<E>** 
- **List<E>** 
- **RandomAccess** 

## Constructors: 
```java 
  import java.util.ArrayList;
  import java.util.Arrays;
  import java.util.Collection;
  import java.util.List;
  
  public class Test {
          public static void main(String[] args) {
                  ArrayList<Integer> a1 = new ArrayList<Integer>(100); // constructing with specified initial capacity 
                  ArrayList<String> a2 = new ArrayList<String>(); // constructs an empty lists with an initial capacity of 10 
                  ArrayList<Integer> a3 = new ArrayList<Integer>(Arrays.asList(1, 2, 3)); // constructs a list containing the elemtns of a specified collection 
          }                                                                                                                                         
  }                                                                                                                                                                   
  
``` 
  
  
  
## Methods: 
```java 
  interface ArrayListMethods<E> {
          boolean add(E e);
  
          void add(int index, E element);
  
          boolean addAll(Collection<? extends E> c);
  
          boolean addAll(int index, Collection<? extends E> c);
  
          void clear();
  
          Object clone();
  
          boolean contains(Object o);
  
          void ensureCapacity(int minCapacity);
  
          void forEach(Consumer<? super E> action);
  
          E get(int index);
  
          int indexOf(Object o);
  
          boolean isEmpty();
  
          Iterator<E> iterator();
  
          int lastIndexOf(Object o);
  
          ListIterator<E> listIterator();
  
          ListIterator<E> listIterator(int index);
  
          E remove(int index);
  
          boolean remove(Object o);
  
          boolean removeAll(Collection<?> c);
  
          boolean removeIf(Predicate<? super E> filter);
  
>>        protected void removeRange(int fromIndex, int toIndex);
  
          void replaceAll(UnaryOperator<E> operator);
  
          boolean retainAll(Collection<?> c);
  
          E set(int index, E element);
  
          int size();
  
          void sort(Comparator<? super E> c);
  
          Spliterator<E> splitIterator();
  
          List<E> subList(int fromIndex, int toIndex);
  
          Object[] toArray();
  
          <T> T[] toArray(T[] a);
  
          void trimToSize();
  }
``` 

# References 
Learn Java. (2022). *Oracle*. <https://dev.java/learn> 

