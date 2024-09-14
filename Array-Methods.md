Certainly! Here’s a comprehensive set of interview questions focused on array manipulation in JavaScript, along with their answers:

### Questions and Answers on Array Manipulation

1. **How can you remove duplicate elements from an array?**
   - **Answer:** You can use a `Set` to remove duplicates because a `Set` only stores unique values. Example:
     ```javascript
     const array = [1, 2, 2, 3, 4, 4, 5];
     const uniqueArray = [...new Set(array)];
     // or
     const uniqueArray = array.filter((value, index, self) => self.indexOf(value) === index);
     ```

2. **How can you flatten a nested array?**
   - **Answer:** Use the `flat()` method to flatten an array to a specified depth. Example:
     ```javascript
     const nestedArray = [1, [2, [3, [4]]]];
     const flattenedArray = nestedArray.flat(2); // Flatten to depth 2
     // or for a deeper flattening:
     const completelyFlattened = nestedArray.flat(Infinity);
     ```

3. **How do you find the maximum value in an array?**
   - **Answer:** You can use the `Math.max()` function along with the spread operator. Example:
     ```javascript
     const numbers = [1, 2, 3, 4, 5];
     const max = Math.max(...numbers);
     ```

4. **How can you remove the first element of an array?**
   - **Answer:** Use the `shift()` method to remove the first element from an array. Example:
     ```javascript
     const array = [1, 2, 3, 4];
     array.shift(); // array is now [2, 3, 4]
     ```

5. **How do you add an element to the end of an array?**
   - **Answer:** Use the `push()` method to add an element to the end of an array. Example:
     ```javascript
     const array = [1, 2, 3];
     array.push(4); // array is now [1, 2, 3, 4]
     ```

6. **How can you combine two arrays into one?**
   - **Answer:** Use the `concat()` method or the spread operator. Example:
     ```javascript
     const array1 = [1, 2, 3];
     const array2 = [4, 5, 6];
     const combined = array1.concat(array2);
     // or
     const combined = [...array1, ...array2];
     ```

7. **How can you find the index of an element in an array?**
   - **Answer:** Use the `indexOf()` method to find the first occurrence of an element. Example:
     ```javascript
     const array = [1, 2, 3, 4];
     const index = array.indexOf(3); // index is 2
     ```

8. **How do you sort an array of numbers in ascending order?**
   - **Answer:** Use the `sort()` method with a compare function. Example:
     ```javascript
     const numbers = [5, 1, 8, 3];
     numbers.sort((a, b) => a - b); // numbers is now [1, 3, 5, 8]
     ```

9. **How can you reverse the order of elements in an array?**
   - **Answer:** Use the `reverse()` method to reverse the order of elements. Example:
     ```javascript
     const array = [1, 2, 3, 4];
     array.reverse(); // array is now [4, 3, 2, 1]
     ```

10. **How can you get a subarray from an array?**
    - **Answer:** Use the `slice()` method to get a subarray. Example:
      ```javascript
      const array = [1, 2, 3, 4, 5];
      const subarray = array.slice(1, 4); // subarray is [2, 3, 4]
      ```

11. **How do you execute a function on each element of an array?**
    - **Answer:** Use the `forEach()` method to execute a function on each element. Example:
      ```javascript
      const array = [1, 2, 3];
      array.forEach(element => console.log(element));
      ```

12. **How can you find an element in an array that satisfies a condition?**
    - **Answer:** Use the `find()` method to return the first element that satisfies the condition. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const found = array.find(element => element > 2); // found is 3
      ```

13. **How do you create a new array with elements that pass a test?**
    - **Answer:** Use the `filter()` method to create a new array with elements that pass the provided test function. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const filtered = array.filter(element => element % 2 === 0); // filtered is [2, 4]
      ```

14. **How can you transform each element of an array into a new value?**
    - **Answer:** Use the `map()` method to transform each element of an array into a new value. Example:
      ```javascript
      const array = [1, 2, 3];
      const mapped = array.map(element => element * 2); // mapped is [2, 4, 6]
      ```

15. **How do you accumulate values in an array into a single result?**
    - **Answer:** Use the `reduce()` method to accumulate values into a single result. Example:
      ```javascript
      const array = [1, 2, 3];
      const sum = array.reduce((accumulator, currentValue) => accumulator + currentValue, 0); // sum is 6
      ```

16. **How can you check if an array contains a specific element?**
    - **Answer:** Use the `includes()` method to check if an array contains a specific element. Example:
      ```javascript
      const array = [1, 2, 3];
      const contains = array.includes(2); // contains is true
      ```

17. **How do you create a new array by concatenating existing arrays or values?**
    - **Answer:** Use the `concat()` method or the spread operator. Example:
      ```javascript
      const array1 = [1, 2];
      const array2 = [3, 4];
      const concatenated = array1.concat(array2); // concatenated is [1, 2, 3, 4]
      // or
      const concatenated = [...array1, ...array2];
      ```

18. **How can you execute a function on each element of an array and collect results?**
    - **Answer:** Use the `map()` method to execute a function on each element and collect the results into a new array. Example:
      ```javascript
      const array = [1, 2, 3];
      const results = array.map(x => x * 2); // results is [2, 4, 6]
      ```

19. **How do you find all elements in an array that match a condition?**
    - **Answer:** Use the `filter()` method to return all elements that match the condition. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const evens = array.filter(x => x % 2 === 0); // evens is [2, 4]
      ```

20. **How can you remove the last element from an array?**
    - **Answer:** Use the `pop()` method to remove the last element from an array. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      array.pop(); // array is now [1, 2, 3]
      ```

21. **How do you find the index of the first occurrence of an element in an array?**
    - **Answer:** Use the `indexOf()` method to find the index of the first occurrence of an element. Example:
      ```javascript
      const array = [1, 2, 3, 2];
      const index = array.indexOf(2); // index is 1
      ```

22. **How can you create a new array by applying a function to each element?**
    - **Answer:** Use the `map()` method to create a new array by applying a function to each element. Example:
      ```javascript
      const numbers = [1, 2, 3];
      const squared = numbers.map(x => x * x); // squared is [1, 4, 9]
      ```

23. **How do you check if at least one element in an array passes a test?**
    - **Answer:** Use the `some()` method to check if at least one element passes the test. Example:
      ```javascript
      const array = [1, 2, 3];
      const hasEven = array.some(x => x % 2 === 0); // hasEven is true
      ```

24. **How can you execute a function for each element of an array and collect a new array?**
    - **Answer:** Use

 the `map()` method to execute a function for each element and collect the results in a new array. Example:
      ```javascript
      const array = [1, 2, 3];
      const doubled = array.map(x => x * 2); // doubled is [2, 4, 6]
      ```

25. **How do you create a shallow copy of an array?**
    - **Answer:** Use the `slice()` method or the spread operator. Example:
      ```javascript
      const array = [1, 2, 3];
      const copy = array.slice(); // or
      const copy = [...array];
      ```

26. **How can you combine multiple arrays into a single array?**
    - **Answer:** Use the `concat()` method or the spread operator. Example:
      ```javascript
      const array1 = [1, 2];
      const array2 = [3, 4];
      const combined = array1.concat(array2); // or
      const combined = [...array1, ...array2];
      ```

27. **How do you create a new array by mapping and flattening?**
    - **Answer:** Use the `flatMap()` method to map and then flatten the result. Example:
      ```javascript
      const array = [1, 2, 3];
      const result = array.flatMap(x => [x, x * 2]); // result is [1, 2, 2, 4, 3, 6]
      ```

28. **How do you find the last index of an element in an array?**
    - **Answer:** Use the `lastIndexOf()` method to find the last index of an element. Example:
      ```javascript
      const array = [1, 2, 3, 2];
      const lastIndex = array.lastIndexOf(2); // lastIndex is 3
      ```

29. **How can you check if all elements in an array pass a test?**
    - **Answer:** Use the `every()` method to check if all elements pass the test. Example:
      ```javascript
      const array = [1, 2, 3];
      const allEven = array.every(x => x % 2 === 0); // allEven is false
      ```

30. **How do you convert an array-like object to a real array?**
    - **Answer:** Use the `Array.from()` method or the spread operator. Example:
      ```javascript
      const arrayLike = {0: 'a', 1: 'b', length: 2};
      const array = Array.from(arrayLike); // or
      const array = [...arrayLike];
      ```

31. **How can you transform an array of objects into an array of specific values?**
    - **Answer:** Use the `map()` method to extract specific values from an array of objects. Example:
      ```javascript
      const array = [{ name: 'Alice' }, { name: 'Bob' }];
      const names = array.map(obj => obj.name); // names is ['Alice', 'Bob']
      ```

32. **How do you remove all instances of a specific value from an array?**
    - **Answer:** Use the `filter()` method to remove all instances of a specific value. Example:
      ```javascript
      const array = [1, 2, 2, 3, 4];
      const filtered = array.filter(x => x !== 2); // filtered is [1, 3, 4]
      ```

33. **How can you get the first few elements of an array?**
    - **Answer:** Use the `slice()` method to get the first few elements. Example:
      ```javascript
      const array = [1, 2, 3, 4, 5];
      const firstThree = array.slice(0, 3); // firstThree is [1, 2, 3]
      ```

34. **How do you add an element to the beginning of an array?**
    - **Answer:** Use the `unshift()` method to add an element to the beginning of an array. Example:
      ```javascript
      const array = [2, 3, 4];
      array.unshift(1); // array is now [1, 2, 3, 4]
      ```

35. **How can you execute a function for each element and get results as an array?**
    - **Answer:** Use the `map()` method to execute a function for each element and get results. Example:
      ```javascript
      const numbers = [1, 2, 3];
      const results = numbers.map(x => x + 1); // results is [2, 3, 4]
      ```

36. **How do you check if an array contains a specific value?**
    - **Answer:** Use the `includes()` method to check if an array contains a specific value. Example:
      ```javascript
      const array = [1, 2, 3];
      const contains = array.includes(2); // contains is true
      ```

37. **How can you replace a value at a specific index in an array?**
    - **Answer:** Directly assign a new value to the specific index. Example:
      ```javascript
      const array = [1, 2, 3];
      array[1] = 4; // array is now [1, 4, 3]
      ```

38. **How do you combine multiple arrays into a single array?**
    - **Answer:** Use the `concat()` method or the spread operator. Example:
      ```javascript
      const array1 = [1, 2];
      const array2 = [3, 4];
      const combined = array1.concat(array2); // combined is [1, 2, 3, 4]
      // or
      const combined = [...array1, ...array2];
      ```

39. **How can you get the last element of an array?**
    - **Answer:** Access the last element using the length of the array. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const lastElement = array[array.length - 1]; // lastElement is 4
      ```

40. **How do you create a new array with elements that do not pass a test?**
    - **Answer:** Use the `filter()` method with the condition reversed. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const notEvens = array.filter(x => x % 2 !== 0); // notEvens is [1, 3]
      ```

41. **How can you make a copy of a portion of an array?**
    - **Answer:** Use the `slice()` method to copy a portion of an array. Example:
      ```javascript
      const array = [1, 2, 3, 4, 5];
      const portion = array.slice(2, 4); // portion is [3, 4]
      ```

42. **How do you remove elements from a specific index in an array?**
    - **Answer:** Use the `splice()` method to remove elements from a specific index. Example:
      ```javascript
      const array = [1, 2, 3, 4, 5];
      array.splice(2, 2); // array is now [1, 2, 5]
      ```

43. **How can you check if all elements in an array are unique?**
    - **Answer:** Convert the array to a `Set` and compare its size with the original array’s length. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const isUnique = new Set(array).size === array.length; // isUnique is true
      ```

44. **How do you execute a function once for each array element and collect results?**
    - **Answer:** Use the `map()` method to execute a function and collect results. Example:
      ```javascript
      const array = [1, 2, 3];
      const results = array.map(x => x * 2); // results is [2, 4, 6]
      ```

45. **How can you sort an array of objects by a specific property?**
    - **Answer:** Use the `sort()` method with a compare function. Example:
      ```javascript
      const array = [{ name: 'Alice', age: 30 }, { name: 'Bob', age: 25 }];
      array.sort((a, b) => a.age - b.age); // array is sorted by age
      ```

46. **How do you concatenate arrays with different lengths?**
    - **Answer:** Use the `concat()` method or spread operator, which works regardless of the arrays' lengths. Example:
      ```javascript
      const array1 = [1, 2];
      const array2 = [3, 4, 5];
      const combined = array1.concat(array2); // combined is [1, 2, 3, 4, 5]
      // or
      const combined = [...array1, ...array2];
      ```

47. **How can you check if an array has a specific length?**
    - **Answer:** Access the `length` property of the array. Example:
      ```javascript
      const array = [1, 2, 3];
      const isLengthThree = array.length === 3; // isLengthThree is true


      ```

48. **How do you remove and return the last element of an array?**
    - **Answer:** Use the `pop()` method, which removes and returns the last element. Example:
      ```javascript
      const array = [1, 2, 3];
      const last = array.pop(); // last is 3, array is now [1, 2]
      ```

49. **How can you find elements in an array that satisfy multiple conditions?**
    - **Answer:** Use the `filter()` method with multiple conditions. Example:
      ```javascript
      const array = [1, 2, 3, 4, 5];
      const result = array.filter(x => x > 2 && x % 2 === 1); // result is [3, 5]
      ```

50. **How do you map an array to an array of arrays?**
    - **Answer:** Use the `map()` method to transform each element into an array. Example:
      ```javascript
      const array = [1, 2, 3];
      const result = array.map(x => [x, x * 2]); // result is [[1, 2], [2, 4], [3, 6]]
      ```

51. **How can you find the minimum value in an array?**
    - **Answer:** Use the `Math.min()` function along with the spread operator. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const min = Math.min(...array); // min is 1
      ```

52. **How do you group elements of an array based on a specific property?**
    - **Answer:** Use the `reduce()` method to group elements based on a property. Example:
      ```javascript
      const array = [{ category: 'A', value: 1 }, { category: 'B', value: 2 }, { category: 'A', value: 3 }];
      const grouped = array.reduce((acc, item) => {
        if (!acc[item.category]) acc[item.category] = [];
        acc[item.category].push(item.value);
        return acc;
      }, {});
      // grouped is { A: [1, 3], B: [2] }
      ```

53. **How can you check if an array contains only a specific type of values?**
    - **Answer:** Use the `every()` method to check if all elements match a specific type. Example:
      ```javascript
      const array = [1, 2, 3];
      const allNumbers = array.every(x => typeof x === 'number'); // allNumbers is true
      ```

54. **How do you create a new array with elements in reversed order?**
    - **Answer:** Use the `reverse()` method to reverse the elements of the array. Example:
      ```javascript
      const array = [1, 2, 3];
      const reversed = array.slice().reverse(); // reversed is [3, 2, 1]
      ```

55. **How can you add an element at a specific position in an array?**
    - **Answer:** Use the `splice()` method to add an element at a specific index. Example:
      ```javascript
      const array = [1, 2, 4];
      array.splice(2, 0, 3); // array is now [1, 2, 3, 4]
      ```

56. **How do you remove a specific element from an array by value?**
    - **Answer:** Use the `filter()` method to remove an element by value. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const result = array.filter(x => x !== 3); // result is [1, 2, 4]
      ```

57. **How can you split an array into chunks of a specific size?**
    - **Answer:** Use the `reduce()` method to split an array into chunks. Example:
      ```javascript
      const array = [1, 2, 3, 4, 5, 6];
      const chunkSize = 2;
      const chunks = array.reduce((result, item, index) => {
        const chunkIndex = Math.floor(index / chunkSize);
        if (!result[chunkIndex]) result[chunkIndex] = [];
        result[chunkIndex].push(item);
        return result;
      }, []);
      // chunks is [[1, 2], [3, 4], [5, 6]]
      ```

58. **How do you merge multiple arrays and remove duplicates?**
    - **Answer:** Use `concat()` or spread operator combined with `Set` to merge arrays and remove duplicates. Example:
      ```javascript
      const array1 = [1, 2, 3];
      const array2 = [2, 3, 4];
      const mergedUnique = [...new Set(array1.concat(array2))];
      // or
      const mergedUnique = [...new Set([...array1, ...array2])];
      ```

59. **How can you find the common elements between two arrays?**
    - **Answer:** Use the `filter()` method combined with `includes()` to find common elements. Example:
      ```javascript
      const array1 = [1, 2, 3];
      const array2 = [2, 3, 4];
      const common = array1.filter(value => array2.includes(value)); // common is [2, 3]
      ```

60. **How do you get the difference between two arrays (elements in one array but not in the other)?**
    - **Answer:** Use the `filter()` method combined with `includes()` to get the difference. Example:
      ```javascript
      const array1 = [1, 2, 3, 4];
      const array2 = [3, 4, 5, 6];
      const difference = array1.filter(value => !array2.includes(value)); // difference is [1, 2]
      ```

61. **How can you find the first element that does not satisfy a condition?**
    - **Answer:** Use the `find()` method with a negated condition. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const firstNotEven = array.find(x => x % 2 !== 0); // firstNotEven is 1
      ```

62. **How do you move an element from one position to another in an array?**
    - **Answer:** Use a combination of `splice()` and `splice()` methods to move an element. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const [moved] = array.splice(1, 1); // Remove element from index 1
      array.splice(2, 0, moved); // Insert element at index 2
      // array is now [1, 3, 2, 4]
      ```

63. **How can you generate an array of numbers from a range?**
    - **Answer:** Use the `Array.from()` method or `map()` to generate an array of numbers from a range. Example:
      ```javascript
      const range = Array.from({ length: 5 }, (_, i) => i + 1); // range is [1, 2, 3, 4, 5]
      // or
      const range = [...Array(5).keys()].map(x => x + 1);
      ```

64. **How do you find the index of the last occurrence of an element in an array?**
    - **Answer:** Use the `lastIndexOf()` method to find the index of the last occurrence. Example:
      ```javascript
      const array = [1, 2, 3, 2];
      const lastIndex = array.lastIndexOf(2); // lastIndex is 3
      ```

65. **How can you check if any elements in an array are equal to a given value?**
    - **Answer:** Use the `some()` method to check if any element is equal to the given value. Example:
      ```javascript
      const array = [1, 2, 3];
      const hasTwo = array.some(x => x === 2); // hasTwo is true
      ```

66. **How do you find the intersection of two arrays (elements that are present in both arrays)?**
    - **Answer:** Use the `filter()` method combined with `includes()` to find the intersection. Example:
      ```javascript
      const array1 = [1, 2, 3];
      const array2 = [2, 3, 4];
      const intersection = array1.filter(value => array2.includes(value)); // intersection is [2, 3]
      ```

67. **How can you get unique values from an array of arrays?**
    - **Answer:** Use `flat()` to flatten the array and then `new Set()` to get unique values. Example:
      ```javascript
      const array = [[1, 2], [2, 3], [4, 5]];
      const uniqueValues = [...new Set(array.flat())]; // uniqueValues is [1, 2, 3, 4, 5]
      ```

68. **How do you find the difference between two arrays of objects based on a property?**
    - **Answer:** Use the `filter()` method with a comparison based on the property. Example:
      ```javascript
      const array1 = [{ id:

 1 }, { id: 2 }];
      const array2 = [{ id: 2 }];
      const difference = array1.filter(obj1 => !array2.some(obj2 => obj1.id === obj2.id));
      // difference is [{ id: 1 }]
      ```

69. **How can you flatten a deeply nested array?**
    - **Answer:** Use the `flat()` method with a depth argument or `flatMap()` for one level. Example:
      ```javascript
      const array = [1, [2, [3, [4]]]];
      const flat = array.flat(3); // flat is [1, 2, 3, 4]
      ```

70. **How do you remove all instances of falsy values from an array?**
    - **Answer:** Use the `filter()` method to remove falsy values. Example:
      ```javascript
      const array = [0, 1, false, 2, '', 3];
      const truthy = array.filter(Boolean); // truthy is [1, 2, 3]
      ```

71. **How can you get the maximum value in an array?**
    - **Answer:** Use the `Math.max()` function along with the spread operator. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const max = Math.max(...array); // max is 4
      ```

72. **How do you get a new array with elements that are different from another array?**
    - **Answer:** Use the `filter()` method to get elements not present in another array. Example:
      ```javascript
      const array1 = [1, 2, 3, 4];
      const array2 = [3, 4, 5, 6];
      const difference = array1.filter(x => !array2.includes(x)); // difference is [1, 2]
      ```

73. **How can you find the first element that satisfies a condition or return a default value?**
    - **Answer:** Use the `find()` method and a default value if not found. Example:
      ```javascript
      const array = [1, 2, 3];
      const found = array.find(x => x > 2) || 'default'; // found is 3
      ```

74. **How do you create an array with a specific length and values?**
    - **Answer:** Use `Array.from()` with a mapping function. Example:
      ```javascript
      const array = Array.from({ length: 3 }, (_, i) => i + 1); // array is [1, 2, 3]
      ```

75. **How can you get the first element in an array that matches a condition?**
    - **Answer:** Use the `find()` method to get the first matching element. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const firstGreaterThanTwo = array.find(x => x > 2); // firstGreaterThanTwo is 3
      ```

76. **How do you merge two arrays without modifying the original arrays?**
    - **Answer:** Use the spread operator or `concat()` to merge without modifying. Example:
      ```javascript
      const array1 = [1, 2];
      const array2 = [3, 4];
      const merged = [...array1, ...array2]; // merged is [1, 2, 3, 4]
      ```

77. **How can you get the values of an array that are present in another array?**
    - **Answer:** Use the `filter()` method with `includes()` to get the common values. Example:
      ```javascript
      const array1 = [1, 2, 3, 4];
      const array2 = [3, 4, 5, 6];
      const commonValues = array1.filter(x => array2.includes(x)); // commonValues is [3, 4]
      ```

78. **How do you iterate over an array of objects and perform an operation?**
    - **Answer:** Use the `forEach()` method to iterate and perform an operation. Example:
      ```javascript
      const array = [{ value: 1 }, { value: 2 }];
      array.forEach(obj => console.log(obj.value)); // logs 1, then 2
      ```

79. **How can you create a new array with elements transformed into a specific format?**
    - **Answer:** Use the `map()` method to transform elements. Example:
      ```javascript
      const array = [1, 2, 3];
      const formatted = array.map(x => `Value: ${x}`); // formatted is ['Value: 1', 'Value: 2', 'Value: 3']
      ```

80. **How do you extract unique elements from a nested array?**
    - **Answer:** Use `flat()` to flatten the array and `new Set()` to extract unique elements. Example:
      ```javascript
      const array = [[1, 2], [2, 3], [4, 5]];
      const unique = [...new Set(array.flat())]; // unique is [1, 2, 3, 4, 5]
      ```

81. **How can you count the occurrences of each element in an array?**
    - **Answer:** Use `reduce()` to count occurrences. Example:
      ```javascript
      const array = [1, 2, 2, 3, 3, 3];
      const count = array.reduce((acc, item) => {
        acc[item] = (acc[item] || 0) + 1;
        return acc;
      }, {});
      // count is { '1': 1, '2': 2, '3': 3 }
      ```

82. **How do you find elements in an array that satisfy a condition and return their indices?**
    - **Answer:** Use `map()` with `filter()` to get indices of elements that satisfy a condition. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const indices = array.map((value, index) => value > 2 ? index : -1).filter(index => index !== -1);
      // indices is [2, 3]
      ```

83. **How can you merge multiple arrays while preserving their order?**
    - **Answer:** Use the spread operator or `concat()` method to merge while preserving order. Example:
      ```javascript
      const array1 = [1, 2];
      const array2 = [3, 4];
      const array3 = [5, 6];
      const merged = [...array1, ...array2, ...array3]; // merged is [1, 2, 3, 4, 5, 6]
      ```

84. **How do you create a new array with each element multiplied by a factor?**
    - **Answer:** Use the `map()` method to multiply each element by a factor. Example:
      ```javascript
      const array = [1, 2, 3];
      const multiplied = array.map(x => x * 2); // multiplied is [2, 4, 6]
      ```

85. **How can you get the last n elements of an array?**
    - **Answer:** Use the `slice()` method with negative indexing to get the last n elements. Example:
      ```javascript
      const array = [1, 2, 3, 4, 5];
      const lastThree = array.slice(-3); // lastThree is [3, 4, 5]
      ```

86. **How do you check if an array contains only numbers?**
    - **Answer:** Use the `every()` method to check if all elements are numbers. Example:
      ```javascript
      const array = [1, 2, 3];
      const onlyNumbers = array.every(x => typeof x === 'number'); // onlyNumbers is true
      ```

87. **How can you find the index of the first occurrence of a specific value in an array?**
    - **Answer:** Use the `indexOf()` method to find the index of the first occurrence. Example:
      ```javascript
      const array = [1, 2, 3, 2];
      const index = array.indexOf(2); // index is 1
      ```

88. **How do you get the difference between two arrays (elements in one but not in the other)?**
    - **Answer:** Use the `filter()` method to find elements that are in one array but not in the other. Example:
      ```javascript
      const array1 = [1, 2, 3, 4];
      const array2 = [3, 4, 5, 6];
      const difference = array1.filter(x => !array2.includes(x)); // difference is [1, 2]
      ```

89. **How do you create a new array from an existing array with some elements removed?**
    - **Answer:** Use the `filter()` method to remove elements based on a condition. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const newArray = array.filter(x => x !== 3); // newArray is [1, 2, 4]
      ```

90. **How can you find the longest string in an array of strings?**
    - **Answer:** Use the `reduce()` method to find the longest string. Example

:
      ```javascript
      const array = ['short', 'medium', 'very long string'];
      const longest = array.reduce((longest, current) => current.length > longest.length ? current : longest, '');
      // longest is 'very long string'
      ```

91. **How do you sort an array of numbers in descending order?**
    - **Answer:** Use the `sort()` method with a custom comparator. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const sortedDescending = array.slice().sort((a, b) => b - a); // sortedDescending is [4, 3, 2, 1]
      ```

92. **How can you transform an array of objects into a dictionary?**
    - **Answer:** Use the `reduce()` method to transform an array into a dictionary. Example:
      ```javascript
      const array = [{ id: 1, name: 'Alice' }, { id: 2, name: 'Bob' }];
      const dictionary = array.reduce((acc, obj) => {
        acc[obj.id] = obj.name;
        return acc;
      }, {});
      // dictionary is { 1: 'Alice', 2: 'Bob' }
      ```

93. **How do you get an array of indices where a condition is met?**
    - **Answer:** Use the `map()` method combined with `filter()` to get indices. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const indices = array.map((value, index) => value % 2 === 0 ? index : -1).filter(index => index !== -1);
      // indices is [1, 3]
      ```

94. **How can you find the most frequent element in an array?**
    - **Answer:** Use `reduce()` to count occurrences and then find the most frequent. Example:
      ```javascript
      const array = [1, 2, 2, 3, 3, 3];
      const frequency = array.reduce((acc, item) => {
        acc[item] = (acc[item] || 0) + 1;
        return acc;
      }, {});
      const mostFrequent = Object.keys(frequency).reduce((a, b) => frequency[a] > frequency[b] ? a : b);
      // mostFrequent is '3'
      ```

95. **How do you shuffle an array?**
    - **Answer:** Use the Fisher-Yates algorithm to shuffle an array. Example:
      ```javascript
      function shuffle(array) {
        for (let i = array.length - 1; i > 0; i--) {
          const j = Math.floor(Math.random() * (i + 1));
          [array[i], array[j]] = [array[j], array[i]]; // Swap elements
        }
        return array;
      }
      ```

96. **How can you determine if two arrays have the same elements?**
    - **Answer:** Use the `every()` method to compare sorted versions of the arrays. Example:
      ```javascript
      const array1 = [1, 2, 3];
      const array2 = [3, 2, 1];
      const isEqual = array1.length === array2.length && array1.sort().every((value, index) => value === array2.sort()[index]);
      // isEqual is true
      ```

97. **How do you extract a section of an array without modifying the original?**
    - **Answer:** Use the `slice()` method to get a section of the array. Example:
      ```javascript
      const array = [1, 2, 3, 4, 5];
      const section = array.slice(1, 4); // section is [2, 3, 4]
      ```

98. **How can you convert an array of strings into a single string?**
    - **Answer:** Use the `join()` method to concatenate array elements into a single string. Example:
      ```javascript
      const array = ['Hello', 'World'];
      const singleString = array.join(' '); // singleString is 'Hello World'
      ```

99. **How do you find the longest consecutive sequence of numbers in an array?**
    - **Answer:** Use a combination of sorting and iteration to find the longest sequence. Example:
      ```javascript
      const array = [1, 2, 3, 5, 6, 7, 8];
      const sorted = array.sort((a, b) => a - b);
      let longest = 0;
      let current = 1;
      for (let i = 1; i < sorted.length; i++) {
        if (sorted[i] === sorted[i - 1] + 1) {
          current++;
        } else {
          longest = Math.max(longest, current);
          current = 1;
        }
      }
      longest = Math.max(longest, current);
      // longest is 4 (sequence [5, 6, 7, 8])
      ```

100. **How can you create a new array with elements replaced by a specified value if they satisfy a condition?**
    - **Answer:** Use the `map()` method to replace elements based on a condition. Example:
      ```javascript
      const array = [1, 2, 3, 4];
      const replaced = array.map(x => x % 2 === 0 ? 'even' : x); // replaced is [1, 'even', 'even', 'even']
      ```