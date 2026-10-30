## 01. Kadane's Algorithm

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/kadanes-algorithm-1587115620/1)

### Problem Description

**Task:** My SubmissionsRefresh Time (IST)StatusMarksLangTest CasesCode2026-07-16 22:26:09Correct4java1120 / 1120View2026-07-16 22:20:19Wrong0java2 / 1120View

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** Not found
- **Expected Auxiliary Space Complexity:** Not found

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-16 22:26:09
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    int maxSubarraySum(int[] arr) {
        // Code here
        int sum =0;
        int maxSum =Integer.MIN_VALUE;
        for(int i =0; i<arr.length; i++){
            sum += arr[i];
            maxSum = Math.max(maxSum , sum);
            if(sum<0) sum =0;
        }
        return maxSum;
    }
}
```

*Generated on: 30/10/2026, 14:48:21*