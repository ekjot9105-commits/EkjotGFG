## 01. Detect Loop in Linked List

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/detect-loop-in-linked-list/1)

### Problem Description

**Task:** Given a singly linked list, find if the given linked list contains a loop or not. A loop exists in a linked list if the next pointer of the last node points to any other node in the list (including itself), rather than being null.Note: Internally, pos(1 based index) is used to denote the position of the node that tail's next pointer is connected to. If pos = 0, it means the last node points to null. Note that pos is not passed as a parameter.Examples:Input: pos = 2, Output: true

#### Examples

##### Example 1

- **Explanation:** There exists a loop as last node is connected back to the first node.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-16 22:32:36
- **Status:** Correct
- **Marks:** 4

```java
/*
class Node {
    int data;
    Node next;

    Node(int x) {
        data = x;
        next = null;
    }
}
*/

class Solution {
    public boolean detectLoop(Node head) {
        // code here
        Node slow = head;
        Node fast = head;
        while(fast != null && fast.next != null){
            fast = fast.next.next;
            slow = slow.next;
            if(slow == fast) return true;
        }
        return false;
    }
}
```

*Generated on: 30/10/2026, 14:47:36*