# Reverse a Linked List 

Given a singly linked list *L* of integers sorted in **ascending order**, return a list of elements sorted in **descending order**. 


**solution** - the natural way of implementing the reversal is through recursion. 

**time**: O(n)

**space**:  O(n) 


## In C++: 
```cpp 
shared_ptr<ListNode<int>> reverseLinkedList(const shared_ptr<ListNode<int>>& head) {
    if (!head || !head->next) {
        return head;
    }
    auto new_head = reverseLinkedList(head->next);
    head->next->next = head;
    head->next = nullptr;
    return new_head;
}
``` 

# References 
Aziz, A. Lee, T. Prakash, A. (2012). *Elements of Programming Interviews* (2nd ed.). <https://www.amazon.com/Elements-Programming-Interviews-Insiders-Guide/dp/1479274836/ref=sr_1_1?crid=OEUQR0809XLT&keywords=elements+of+programming+interviews+c%2B%2B&qid=1670799488&sprefix=elements+of+programming+in%2Caps%2C86&sr=8-1> 
