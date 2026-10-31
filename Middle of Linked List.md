## 01. Middle of Linked List

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/finding-middle-element-in-a-linked-list/1)

### Problem Description

**Task:** My SubmissionsRefresh Time (IST)StatusMarksLangTest CasesCode2026-07-16 22:43:33Correct2java1115 / 1115View

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** Not found
- **Expected Auxiliary Space Complexity:** Not found

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-16 22:43:33
- **Status:** Correct
- **Marks:** 2

```java
/*
class Node {
    int data;
    Node next;

    Node(int x) {
        data = x;
        next = null;
    }
} */

class Solution {
    int getMiddle(Node head) {
        // code here
        Node slow = head; 
        Node fast = head;
        while(fast != null && fast.next != null){
            fast = fast.next.next;
            slow = slow.next;
        }
        return slow.data;
    }
}
```

*Generated on: 31/10/2026, 14:11:56*