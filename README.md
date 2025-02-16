# Writing-Test-Specifications
Block 18

**Unit Tests:**

1. A function called "multiplication" that returns the product of the two input numbers.
**1. Test for positive integers**
Input: Two positive integers, for example, 3 and 5.
Expected Output: The product of the two integers (3 * 5 = 15).
Purpose: To ensure the function handles and returns correct results for two positive numbers.
**2. Test for negative integers**
Input: Two negative integers, for example, -4 and -6.
Expected Output: The product of the two integers (-4 * -6 = 24).
Purpose: To ensure the function correctly handles the multiplication of two negative numbers, which should return a positive product.
**3. Test for multiplication of a positive and negative integer**
Input: One positive and one negative integer, for example, 7 and -2.
Expected Output: The product of the two integers (7 * -2 = -14).
Purpose: To test that the function handles the multiplication of one positive and one negative integer, which should return a negative product.
**4. Test for multiplication by zero**
Input: Any number and zero, for example, 8 and 0.
Expected Output: Zero (8 * 0 = 0).
Purpose: To verify that multiplying any number by zero results in zero.
**5. Test for multiplication by one**
Input: Any number and one, for example, 5 and 1.
Expected Output: The same number (5 * 1 = 5).
Purpose: To ensure the function correctly handles multiplication by one, which should return the original number.
**6. Test for floating-point numbers**
Input: Two floating-point numbers, for example, 2.5 and 4.2.
Expected Output: The product of the numbers (2.5 * 4.2 = 10.5).
Purpose: To ensure the function can handle and return correct results when dealing with floating-point numbers.
**7. Test for large numbers**
Input: Two very large numbers, for example, 1000000 and 5000000.
Expected Output: The correct product (1000000 * 5000000 = 5000000000000).
Purpose: To test that the function handles large numbers without errors or overflow.
**8. Test for very small numbers (close to zero)**
Input: Two small numbers, for example, 0.0001 and 10000.
Expected Output: The product of the numbers (0.0001 * 10000 = 1).
Purpose: To verify that the function handles small decimal values correctly.
**9. Test for equal inputs**
Input: Two identical numbers, for example, 6 and 6.
Expected Output: The square of the number (6 * 6 = 36).
Purpose: To check that the function handles cases where both input numbers are the same.
**10. Test for non-numeric input (invalid case)**
Input: Non-numeric values, such as strings or other data types.
Expected Output: An error or appropriate exception (e.g., TypeError).
Purpose: To ensure the function raises an appropriate error when non-numeric values are passed.

2. A function called "concatOdds" takes two arrays of integers as arguments. It should return a single array that only contains the odd numbers, in ascending order, from both of the arrays.
**1. Test for arrays containing only odd numbers**
Input: Two arrays of odd numbers, for example, [3, 5, 7] and [9, 11, 13].
Expected Output: A single array containing all the odd numbers from both arrays, sorted in ascending order (e.g., [3, 5, 7, 9, 11, 13]).
Purpose: To verify that the function correctly identifies and merges all odd numbers from two arrays in sorted order.
**2. Test for arrays containing only even numbers**
Input: Two arrays of even numbers, for example, [2, 4, 6] and [8, 10, 12].
Expected Output: An empty array, since no odd numbers exist in either array (e.g., []).
Purpose: To check that the function returns an empty array when there are no odd numbers.
**3. Test for arrays containing a mix of odd and even numbers**
Input: Arrays with both even and odd numbers, for example, [3, 2, 1] and [9, 1, 1, 1, 4, 15, -1].
Expected Output: A merged, sorted array of only the odd numbers from both arrays (e.g., [-1, 1, 3, 9, 15]).
Purpose: To ensure the function correctly filters out even numbers and returns only the odd numbers from both arrays, sorted.
**4. Test for duplicates of the same odd number**
Input: Arrays containing duplicates of the same odd number, for example, [1, 3, 3, 1] and [9, 1, 15, 1].
Expected Output: A sorted array with unique odd numbers (e.g., [1, 3, 9, 15]).
Purpose: To ensure the function removes duplicates of odd numbers and returns only unique values, as shown in the example provided.
**5. Test for negative odd numbers**
Input: Arrays containing negative odd numbers, for example, [-3, -5, -7] and [1, -1, 3].
Expected Output: A sorted array containing the odd numbers, including negative ones (e.g., [-7, -5, -3, -1, 1, 3]).
Purpose: To check that the function properly handles negative odd numbers.
**6. Test for empty arrays**
Input: Two empty arrays, [] and [].
Expected Output: An empty array, as there are no odd numbers in either array (e.g., []).
Purpose: To ensure the function works when no data is provided, returning an empty result.
**7. Test for one empty array and one non-empty array**
Input: One empty array and one array with odd and even numbers, for example, [] and [1, 2, 3, 4, 5].
Expected Output: An array with only the odd numbers from the non-empty array, sorted (e.g., [1, 3, 5]).
Purpose: To check that the function correctly processes when one array is empty.
**8. Test for non-array inputs**
Input: Non-array arguments, such as strings or numbers, for example, 'string' and 42.
Expected Output: An error or exception (e.g., TypeError) indicating that the inputs are invalid.
Purpose: To ensure the function properly handles invalid inputs and raises appropriate errors.
**9. Test for arrays with mixed data types (e.g., numbers and strings)**
Input: Arrays that contain both integers and other data types, for example, [1, 'a', 3, 5] and [7, 9, 'b'].
Expected Output: An array of only the odd numbers, with invalid data types excluded (e.g., [1, 3, 5, 7, 9]).
Purpose: To check if the function can handle mixed data types and exclude non-integer elements.
**10. Test for arrays of different lengths**
Input: Two arrays of different lengths, for example, [1, 3, 5] and [9, 7].
Expected Output: A merged, sorted array of odd numbers (e.g., [1, 3, 5, 7, 9]).
Purpose: To test that the function can handle arrays of different sizes and still return the correct result.
