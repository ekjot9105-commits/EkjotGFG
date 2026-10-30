## 01. Majority Element

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/majority-element-1587115620/1)

### Problem Description

**Task:** Given an array arr[]. Find the majority element in the array. If no majority element exists, return -1.Note: A majority element in an array is an element that appears strictly more than arr.size()/2 times in the array.Examples:Input: arr[] = [1, 1, 2, 1, 3, 5, 1]

#### Examples

##### Example 1

- **Output:**
```text
-1
```
- **Explanation:** Since, no element is present more than 2/2 times, so there is no majority element.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-17 21:24:10
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    int majorityElement(int arr[]) {
        // code here
        int candidate =0;
        int count =0;
        for(int num : arr){
            if(count ==0){
                candidate = num;
            }
            if(candidate == num ){
                count++;
            }else count--;
        }
        count =0;
        for(int num : arr){
            if(candidate == num){
                count++;
            }
        }
        return count>arr.length/2?candidate:-1;
    }
}
```

*Generated on: 30/10/2026, 14:46:04*