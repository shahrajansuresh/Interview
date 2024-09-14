 list of array-related questions ranging from basic to advanced levels, commonly asked in interviews. Each question is followed by a brief description and a sample solution.

### **Basic Questions**

1. **Find the Largest Element in an Array**
   - **Question:** Given an array of integers, find the largest element.
   - **Example:** `[3, 5, 7, 2, 8]`
   - **Solution:**
     ```javascript
     function findLargestElement(arr) {
       return Math.max(...arr);
     }

     console.log(findLargestElement([3, 5, 7, 2, 8])); // Output: 8
     ```

2. **Find the Sum of Elements in an Array**
   - **Question:** Given an array of integers, find the sum of all elements.
   - **Example:** `[1, 2, 3, 4]`
   - **Solution:**
     ```javascript
     function sumOfElements(arr) {
       return arr.reduce((sum, num) => sum + num, 0);
     }

     console.log(sumOfElements([1, 2, 3, 4])); // Output: 10
     ```

3. **Check if an Array Contains a Specific Element**
   - **Question:** Check if a given array contains a specific element.
   - **Example:** `[1, 2, 3, 4]`, `3`
   - **Solution:**
     ```javascript
     function containsElement(arr, element) {
       return arr.includes(element);
     }

     console.log(containsElement([1, 2, 3, 4], 3)); // Output: true
     ```

4. **Reverse an Array**
   - **Question:** Reverse the elements of an array.
   - **Example:** `[1, 2, 3, 4]`
   - **Solution:**
     ```javascript
     function reverseArray(arr) {
       return arr.reverse();
     }

     console.log(reverseArray([1, 2, 3, 4])); // Output: [4, 3, 2, 1]
     ```

5. **Remove Duplicates from an Array**
   - **Question:** Remove duplicates from an array.
   - **Example:** `[1, 2, 2, 3, 4, 4]`
   - **Solution:**
     ```javascript
     function removeDuplicates(arr) {
       return [...new Set(arr)];
     }

     console.log(removeDuplicates([1, 2, 2, 3, 4, 4])); // Output: [1, 2, 3, 4]
     ```

### **Intermediate Questions**

6. **Find the Second Largest Element in an Array**
   - **Question:** Find the second largest element in an array.
   - **Example:** `[10, 5, 20, 8]`
   - **Solution:**
     ```javascript
     function secondLargest(arr) {
       let first = -Infinity;
       let second = -Infinity;

       for (const num of arr) {
         if (num > first) {
           second = first;
           first = num;
         } else if (num > second && num < first) {
           second = num;
         }
       }

       return second;
     }

     console.log(secondLargest([10, 5, 20, 8])); // Output: 10
     ```

7. **Find the Intersection of Two Arrays**
   - **Question:** Find the common elements between two arrays.
   - **Example:** `[1, 2, 3, 4]` and `[3, 4, 5, 6]`
   - **Solution:**
     ```javascript
     function intersection(arr1, arr2) {
       return arr1.filter(value => arr2.includes(value));
     }

     console.log(intersection([1, 2, 3, 4], [3, 4, 5, 6])); // Output: [3, 4]
     ```

8. **Move All Zeroes to the End of an Array**
   - **Question:** Move all zeroes in an array to the end without changing the order of non-zero elements.
   - **Example:** `[0, 1, 0, 3, 12]`
   - **Solution:**
     ```javascript
     function moveZeroes(arr) {
       let lastNonZeroFoundAt = 0;
       for (let i = 0; i < arr.length; i++) {
         if (arr[i] !== 0) {
           [arr[lastNonZeroFoundAt], arr[i]] = [arr[i], arr[lastNonZeroFoundAt]];
           lastNonZeroFoundAt++;
         }
       }
     }

     const arr = [0, 1, 0, 3, 12];
     moveZeroes(arr);
     console.log(arr); // Output: [1, 3, 12, 0, 0]
     ```

9. **Find the Majority Element (Boyer-Moore Voting Algorithm)**
   - **Question:** Given an array, find the majority element (an element that appears more than `n/2` times).
   - **Example:** `[3, 2, 3]`
   - **Solution:**
     ```javascript
     function majorityElement(nums) {
       let count = 0;
       let candidate = null;
       
       for (const num of nums) {
         if (count === 0) {
           candidate = num;
         }
         count += (num === candidate) ? 1 : -1;
       }
       
       return candidate;
     }

     console.log(majorityElement([3, 2, 3])); // Output: 3
     ```

10. **Find the Missing Number in an Array**
    - **Question:** Given an array containing `n` distinct numbers taken from `0, 1, 2, ..., n`, find the one that is missing from the array.
    - **Example:** `[3, 0, 1]`
    - **Solution:**
      ```javascript
      function findMissingNumber(arr) {
        const n = arr.length;
        const totalSum = (n * (n + 1)) / 2;
        const arraySum = arr.reduce((sum, num) => sum + num, 0);
        
        return totalSum - arraySum;
      }

      console.log(findMissingNumber([3, 0, 1])); // Output: 2
      ```

### **Advanced Questions**

11. **Rotate a Matrix by 90 Degrees**
    - **Question:** Given an `n x n` matrix, rotate it by 90 degrees clockwise.
    - **Example:** `[[1, 2, 3], [4, 5, 6], [7, 8, 9]]`
    - **Solution:**
      ```javascript
      function rotateMatrix(matrix) {
        const n = matrix.length;
        for (let i = 0; i < n; i++) {
          for (let j = i; j < n; j++) {
            [matrix[i][j], matrix[j][i]] = [matrix[j][i], matrix[i][j]];
          }
        }
        
        for (let i = 0; i < n; i++) {
          matrix[i].reverse();
        }
      }

      const matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
      rotateMatrix(matrix);
      console.log(matrix); // Output: [[7, 4, 1], [8, 5, 2], [9, 6, 3]]
      ```

12. **Find All Unique Triplets in an Array that Sum to Zero (3-Sum Problem)**
    - **Question:** Given an array of integers, find all unique triplets that sum up to zero.
    - **Example:** `[-1, 0, 1, 2, -1, -4]`
    - **Solution:**
      ```javascript
      function threeSum(nums) {
        const result = [];
        nums.sort((a, b) => a - b);
        
        for (let i = 0; i < nums.length - 2; i++) {
          if (i > 0 && nums[i] === nums[i - 1]) continue;
          
          let left = i + 1;
          let right = nums.length - 1;
          
          while (left < right) {
            const sum = nums[i] + nums[left] + nums[right];
            
            if (sum === 0) {
              result.push([nums[i], nums[left], nums[right]]);
              while (left < right && nums[left] === nums[left + 1]) left++;
              while (left < right && nums[right] === nums[right - 1]) right--;
              left++;
              right--;
            } else if (sum < 0) {
              left++;
            } else {
              right--;
            }
          }
        }
        
        return result;
      }

      console.log(threeSum([-1, 0, 1, 2, -1, -4])); // Output: [[-1, -1, 2], [-1, 0, 1]]
      ```

13. **Find the Maximum Product of Two Integers in an Array**
    - **Question:** Given an array of integers, find the maximum product of any two integers.
    - **Example:** `[1, 10, 2, 

6, 5]`
    - **Solution:**
      ```javascript
      function maxProductOfTwo(arr) {
        let max1 = -Infinity;
        let max2 = -Infinity;
        
        for (const num of arr) {
          if (num > max1) {
            max2 = max1;
            max1 = num;
          } else if (num > max2) {
            max2 = num;
          }
        }
        
        return max1 * max2;
      }

      console.log(maxProductOfTwo([1, 10, 2, 6, 5])); // Output: 60
      ```

14. **Find the Longest Increasing Subsequence**
    - **Question:** Given an integer array, find the length of the longest increasing subsequence.
    - **Example:** `[10, 9, 2, 5, 3, 7, 101, 18]`
    - **Solution:**
      ```javascript
      function lengthOfLIS(nums) {
        if (nums.length === 0) return 0;
        
        const dp = new Array(nums.length).fill(1);
        
        for (let i = 1; i < nums.length; i++) {
          for (let j = 0; j < i; j++) {
            if (nums[i] > nums[j]) {
              dp[i] = Math.max(dp[i], dp[j] + 1);
            }
          }
        }
        
        return Math.max(...dp);
      }

      console.log(lengthOfLIS([10, 9, 2, 5, 3, 7, 101, 18])); // Output: 4
      ```

15. **Find the Minimum Window Substring Containing All Characters**
    - **Question:** Given a string `s` and a string `t`, find the minimum window in `s` which will contain all the characters in `t`.
    - **Example:** `s = "ADOBECODEBANC"`, `t = "ABC"`
    - **Solution:**
      ```javascript
      function minWindow(s, t) {
        if (t.length > s.length) return "";

        const tCount = {};
        const sCount = {};
        for (const char of t) tCount[char] = (tCount[char] || 0) + 1;

        let left = 0;
        let right = 0;
        let minLen = Infinity;
        let minWindow = "";
        
        while (right < s.length) {
          const charRight = s[right];
          sCount[charRight] = (sCount[charRight] || 0) + 1;

          while (containsAll(sCount, tCount)) {
            if (right - left + 1 < minLen) {
              minLen = right - left + 1;
              minWindow = s.substring(left, right + 1);
            }
            const charLeft = s[left];
            sCount[charLeft]--;
            if (sCount[charLeft] === 0) delete sCount[charLeft];
            left++;
          }
          
          right++;
        }

        return minWindow;
      }

      function containsAll(sCount, tCount) {
        for (const char in tCount) {
          if (sCount[char] < tCount[char]) return false;
        }
        return true;
      }

      console.log(minWindow("ADOBECODEBANC", "ABC")); // Output: "BANC"
      ```
Certainly! Here are some common Data Structures and Algorithms (DSA) related logical questions focusing on array manipulation, along with their solutions. These types of questions are frequently asked in technical interviews in India.

### **1. Find the Maximum Subarray Sum (Kadane’s Algorithm)**

**Question:** Given an array of integers, find the contiguous subarray with the maximum sum.

**Example:**
```javascript
const arr = [-2, 1, -3, 4, -1, 2, 1, -5, 4];
```

**Solution:**
```javascript
function maxSubarraySum(arr) {
  let maxSoFar = arr[0];
  let maxEndingHere = arr[0];
  
  for (let i = 1; i < arr.length; i++) {
    maxEndingHere = Math.max(arr[i], maxEndingHere + arr[i]);
    maxSoFar = Math.max(maxSoFar, maxEndingHere);
  }
  
  return maxSoFar;
}

console.log(maxSubarraySum([-2, 1, -3, 4, -1, 2, 1, -5, 4])); // Output: 6
```

### **2. Find the First Missing Positive Integer**

**Question:** Given an unsorted integer array, find the smallest missing positive integer.

**Example:**
```javascript
const arr = [3, 4, -1, 1];
```

**Solution:**
```javascript
function firstMissingPositive(nums) {
  let n = nums.length;

  for (let i = 0; i < n; i++) {
    while (nums[i] > 0 && nums[i] <= n && nums[nums[i] - 1] !== nums[i]) {
      [nums[i], nums[nums[i] - 1]] = [nums[nums[i] - 1], nums[i]];
    }
  }

  for (let i = 0; i < n; i++) {
    if (nums[i] !== i + 1) {
      return i + 1;
    }
  }

  return n + 1;
}

console.log(firstMissingPositive([3, 4, -1, 1])); // Output: 2
```

### **3. Rotate Array**

**Question:** Given an array and a number `k`, rotate the array to the right by `k` steps.

**Example:**
```javascript
const arr = [1, 2, 3, 4, 5, 6, 7];
const k = 3;
```

**Solution:**
```javascript
function rotateArray(nums, k) {
  k = k % nums.length; // Handle cases where k > nums.length
  reverse(nums, 0, nums.length - 1);
  reverse(nums, 0, k - 1);
  reverse(nums, k, nums.length - 1);
}

function reverse(nums, start, end) {
  while (start < end) {
    [nums[start], nums[end]] = [nums[end], nums[start]];
    start++;
    end--;
  }
}

const arr = [1, 2, 3, 4, 5, 6, 7];
rotateArray(arr, 3);
console.log(arr); // Output: [5, 6, 7, 1, 2, 3, 4]
```

### **4. Merge Intervals**

**Question:** Given a collection of intervals, merge all overlapping intervals.

**Example:**
```javascript
const intervals = [[1, 3], [2, 6], [8, 10], [15, 18]];
```

**Solution:**
```javascript
function mergeIntervals(intervals) {
  if (intervals.length === 0) return [];
  
  intervals.sort((a, b) => a[0] - b[0]);
  
  const merged = [intervals[0]];
  
  for (let i = 1; i < intervals.length; i++) {
    const lastMerged = merged[merged.length - 1];
    const current = intervals[i];
    
    if (lastMerged[1] >= current[0]) {
      lastMerged[1] = Math.max(lastMerged[1], current[1]);
    } else {
      merged.push(current);
    }
  }
  
  return merged;
}

console.log(mergeIntervals([[1, 3], [2, 6], [8, 10], [15, 18]])); // Output: [[1, 6], [8, 10], [15, 18]]
```

### **5. Find the Majority Element**

**Question:** Given an array, find the majority element (the element that appears more than `n/2` times). Assume that the majority element always exists.

**Example:**
```javascript
const arr = [3, 2, 3];
```

**Solution:**
```javascript
function majorityElement(nums) {
  let count = 0;
  let candidate = null;
  
  for (const num of nums) {
    if (count === 0) {
      candidate = num;
    }
    count += (num === candidate) ? 1 : -1;
  }
  
  return candidate;
}

console.log(majorityElement([3, 2, 3])); // Output: 3
```

### **6. Find Duplicates in an Array**

**Question:** Given an array of integers where each integer is between `1` and `n` (inclusive), find all the duplicates in the array.

**Example:**
```javascript
const arr = [4, 3, 2, 7, 8, 2, 1, 5, 6, 3];
```

**Solution:**
```javascript
function findDuplicates(nums) {
  const result = [];
  
  for (const num of nums) {
    const index = Math.abs(num) - 1;
    if (nums[index] < 0) {
      result.push(index + 1);
    } else {
      nums[index] = -nums[index];
    }
  }
  
  return result;
}

console.log(findDuplicates([4, 3, 2, 7, 8, 2, 1, 5, 6, 3])); // Output: [2, 3]
```

### **7. Two Sum**

**Question:** Given an array of integers and a target sum, find two numbers such that they add up to the target sum.

**Example:**
```javascript
const nums = [2, 7, 11, 15];
const target = 9;
```

**Solution:**
```javascript
function twoSum(nums, target) {
  const map = new Map();
  
  for (let i = 0; i < nums.length; i++) {
    const complement = target - nums[i];
    if (map.has(complement)) {
      return [map.get(complement), i];
    }
    map.set(nums[i], i);
  }
  
  return [];
}

console.log(twoSum([2, 7, 11, 15], 9)); // Output: [0, 1]
```

### **8. Move Zeroes**

**Question:** Given an array, move all zeros to the end without changing the order of non-zero elements.

**Example:**
```javascript
const arr = [0, 1, 0, 3, 12];
```

**Solution:**
```javascript
function moveZeroes(nums) {
  let lastNonZeroFoundAt = 0;
  
  for (let i = 0; i < nums.length; i++) {
    if (nums[i] !== 0) {
      [nums[lastNonZeroFoundAt], nums[i]] = [nums[i], nums[lastNonZeroFoundAt]];
      lastNonZeroFoundAt++;
    }
  }
}

const arr = [0, 1, 0, 3, 12];
moveZeroes(arr);
console.log(arr); // Output: [1, 3, 12, 0, 0]
```

### **9. Product of Array Except Self**

**Question:** Given an array `nums`, return an array `output` where `output[i]` is the product of all the numbers in `nums` except `nums[i]`.

**Example:**
```javascript
const arr = [1, 2, 3, 4];
```

**Solution:**
```javascript
function productExceptSelf(nums) {
  const length = nums.length;
  const left = Array(length).fill(1);
  const right = Array(length).fill(1);
  const result = Array(length);

  left[0] = 1;
  for (let i = 1; i < length; i++) {
    left[i] = left[i - 1] * nums[i - 1];
  }
  
  right[length - 1] = 1;
  for (let i = length - 2; i >= 0; i--) {
    right[i] = right[i + 1] * nums[i + 1];
  }
  
  for (let i = 0; i < length; i++) {
    result[i] = left[i] * right[i];
  }
  
  return result;
}

console.log(productExceptSelf([1, 2, 3, 4])); // Output: [24, 12, 8, 6]
```

### **10. Longest Consecutive Sequence**

**Question:** Given an unsorted array of integers, find the length of the longest consecutive elements sequence.

**

Example:**
```javascript
const arr = [100, 4, 200, 1, 3, 2];
```

**Solution:**
```javascript
function longestConsecutive(nums) {
  const set = new Set(nums);
  let longest = 0;

  for (const num of set) {
    if (!set.has(num - 1)) {
      let currentNum = num;
      let currentStreak = 1;

      while (set.has(currentNum + 1)) {
        currentNum += 1;
        currentStreak += 1;
      }

      longest = Math.max(longest, currentStreak);
    }
  }

  return longest;
}

console.log(longestConsecutive([100, 4, 200, 1, 3, 2])); // Output: 4
```
