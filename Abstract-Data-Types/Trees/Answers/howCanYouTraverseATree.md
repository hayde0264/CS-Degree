# How can you traverse a tree? 

## For example: 
```java 
  class BinaryTreeNode<T> {                                                     
          public T data;                                                        
          public BinaryTreeNode<T> left, right;                                 
  }                                                                             
  
  class Test {                                                                  
          public static void treeTraversal(BinaryTreeNode<Integer> root) { 
                  if (root != null) {                                           
                          System.out.println("Preorder: " + root.data);         
                  treeTraversal(root.left);                                     
                          System.out.println("Inorder: " + root.data);          
                  treeTraversal(root.right);                                    
       
                  System.out.println("Postorder: " + root.data);
                  }                                      
          }
  } 
``` 

# References 
# References 
Aziz, A. Lee, T. Prakash, A. (2015). *Elements of Programming Interviews in Java* (1st ed.). <https://www.amazon.com/Elements-Programming-Interviews-Questions-Tsung-Hsien/dp/B00C7F0V3W/ref=sr_1_1?crid=SU7GU68QNL5N&keywords=elements+of+programming+interviews+in+java+1st+edition&qid=1669594847&sprefix=elements+of+programming+interviews+in+java+1st+edition+%2Caps%2C72&sr=8-1> 
