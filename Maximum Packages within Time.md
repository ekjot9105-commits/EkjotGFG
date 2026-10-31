## 01. Maximum Packages within Time

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/bird-and-maximum-fruit-gathering0509/1?_gl=1*g8tgqf*_up*MQ..*_gs*MQ..&gclid=CjwKCAjwo5bXBhAEEiwAkgpgXNPP5rDJa8XI1z63VR9UUIwnPb-eTb3pr89Gamtj5DogB76eGUfGShoCnu0QAvD_BwE&gbraid=0AAAAAC9yBkB2KcBPkC2i9loTl1_gBa0fS)

### Problem Description

**Task:** A delivery agent has to deliver packages at locations arranged in a line. The number of packages at the ith location is given by arr[i]. The agent can start at any location and can only visit consecutive locations.Visiting each location takes 1 unit of time.Given arr[] and totalTime, find the maximum number of packages the agent can deliver within totalTime.Examples:Input: arr[] = [2, 1, 3, 5, 0, 1, 4], totalTime = 3

#### Examples

##### Example 1

- **Output:**
```text
8
```
- **Explanation:** The agent can visit two consecutive locations. Starting from the second location, it delivers arr[1] + arr[2] = 6 + 2 = 8 packages. Starting from the fourth location gives arr[3] + arr[4] = 5 + 3 = 8 packages. Hence, the maximum is 8 packages.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 14:10:21
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public int maxPackages(int[] arr, int totalTime) {

        int n = arr.length;
        int k = Math.min(n, totalTime);

        int sum = 0;

        for (int i = 0; i < k; i++) {
            sum += arr[i];
        }

        int ans = sum;


        for (int i = k; i < n; i++) {

            sum += arr[i];       
            sum -= arr[i - k];   
            ans = Math.max(ans, sum);
        }

        return ans;
    }
}
```

*Generated on: 31/10/2026, 14:11:20*