Array Operations
Problem 1: Sum of Distinct Elements
Description
Given two sets of elements, find the sum of all distinct elements from the set. The output should include the sum of elements that are present in either of the given sets.

Solution
The solution utilizes arrays to store distinct elements and calculates the sum.

Algorithm
Initialize sum to 0.
Compare each element of set one with the second set. If the element is not present, add it to the distinct elements array.
Perform the vice versa to add elements from the second set.
Calculate the sum of distinct elements.

function findSumOfDistinctElements(arr1, arr2) {
  let distinctElements = [];

  for (let element of arr1) {
    if (!arr2.includes(element)) {
      distinctElements.push(element);
    }
  }

  for (let element of arr2) {
    if (!arr1.includes(element)) {
      distinctElements.push(element);
    }
  }

  let sum = distinctElements.reduce((acc, curr) => acc + curr, 0);
  return sum;
}

// Example usage
let arr1 = [3, 1, 7, 9];
let arr2 = [2, 4, 1, 9, 3];
let result = findSumOfDistinctElements(arr1, arr2);
console.log(`Output: ${result}`);

Problem 2: Dot Product and Orthogonality Check
Description
Calculate the dot product of two vectors and determine if they are orthogonal. The dot product of two orthogonal vectors is zero.

Solution
The solution provides functions to calculate the dot product and check for orthogonality using JavaScript arrays.

Algorithm
Implement a function dotProduct to calculate the dot product of two vectors.
Implement a function areVectorsOrthogonal to check if two vectors are orthogonal using the dot product.
Use these functions to determine orthogonality for n pairs of vectors.

// Example vectors
let vector1 = [1, 2, 3];
let vector2 = [4, -2, 1];

// Calculate dot product and check for orthogonality
let result = areVectorsOrthogonal(vector1, vector2);
console.log(`Are vectors orthogonal? ${result}`);