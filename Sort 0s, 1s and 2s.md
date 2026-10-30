## 01. Sort 0s, 1s and 2s

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/sort-an-array-of-0s-1s-and-2s4231/1)

### Problem Description

**Task:** Given an array arr[] containing only 0s, 1s, and 2s. Sort the array in ascending order. Examples:Input: arr[] = [0, 1, 2, 0, 1, 2]

#### Examples

##### Example 1

- **Output:**
```text
[0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 2, 2]
```
- **Explanation:** 0s, 1s and 2s are segregated into ascending order.Follow up: Could you come up with a one-pass algorithm using only constant extra space?

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-14 17:30:34
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
	public void sort012(int[] arr) {
		// code here
		int zeros = 0;
		int one = 0;
		int two = 0;
		for (int num : arr) {
			if (num == 0)zeros++;
			if (num == 1)
				one++;
			if (num == 2)two++;
		}
		for (int i = 0; i<zeros; i++) {
			arr[i] = 0;
		}
		for (int i = zeros; i<one+zeros; i++) {
			arr[i] = 1;
		}
		for (int i = one+zeros; i<two+one+zeros; i++) {
			arr[i] = 2;
		}

	}
}
```

*Generated on: 30/10/2026, 14:49:13*