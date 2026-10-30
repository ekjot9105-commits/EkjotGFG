## 01. Sort Two Parts Sorted

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/sort-the-half-sorted2157/1)

### Problem Description

**Task:** Given an integer array arr[] where the two parts around a break point are individually sorted, merge them into a single sorted array. The break point can be anywhere in the array, including at the beginning or end.Examples:Input: arr[] = [2, 3, 8, -1, 7, 10]

#### Examples

##### Example 1

- **Output:**
```text
[10, 20, 30]
```
- **Explanation:** One part is empty and the other part is whole array which is already sorted.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-11 11:46:07
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public void mergeTwoParts(int[] arr) {
        // code here
        Arrays.sort(arr);
    }
}
```

*Generated on: 30/10/2026, 14:39:51*