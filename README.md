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

**Functional Tests:**
1. A shopping cart checkout feature that allows a user to check out as a guest (without an account), or as a logged-in user. They should be allowed to do either, but should be asked if they want to create an account or log in if they check out as a guest.

_Assumptions:_
**Guest Checkout:**
If a user selects guest checkout, they will be prompted to either log in or create an account after entering their details (such as shipping and billing information).
**Logged-in User Checkout:**
If the user is already logged in, the checkout process will proceed without asking them to log in again.
**Empty Cart:**
If the shopping cart is empty, the system should prevent the checkout process and display a message like "Your cart is empty. Please add items to your cart before proceeding."
**User Feedback During Checkout:**
The system should provide feedback to the user at each step of the checkout process, including:
An initial cart summary with items listed.
A payment method section (credit card, PayPal, etc.).
A shipping information section (address, shipping method).
A final confirmation before submitting the order.
**Test Input:**
A user with an empty shopping cart, attempting to check out as both a guest and a logged-in user.

_Test Scenario 1: Guest Checkout with Items in the Cart_
**Test Steps:**
Add items to the shopping cart (e.g., two items worth $20 and $30).
Proceed to checkout as a guest.
The system should display a message asking the user to log in or create an account (e.g., "Would you like to log in or create an account to save your information for future purchases?").
Select "Proceed as Guest" and enter the required shipping and billing information.
The system should then show a summary of the order, including the items in the cart, total price, shipping details, and payment options.
After reviewing the order, the system should ask for confirmation before finalizing the purchase.
Expected Behavior:
If the cart is not empty, the user should be able to proceed with checkout after entering shipping and payment information.
The system should not prompt for login if the user chooses to continue as a guest, but should still allow the option to create an account.
Expected Output:
The system allows the guest user to proceed with checkout without an account, while prompting them to create an account after completing the purchase.

_Test Scenario 2: Logged-in User Checkout_
**Test Steps:**
Log in to the system with a registered account.
Add items to the shopping cart (e.g., two items worth $50 and $25).
Proceed to checkout as a logged-in user.
The system should skip the account creation/login prompt, as the user is already logged in.
The user should enter their shipping and payment details and review the order.
The system should allow the user to confirm the purchase and proceed with checkout.
Expected Behavior:
The user is already logged in, so no prompts to log in or create an account should appear.
The checkout process should proceed smoothly, with the user able to enter shipping details, review the order, and confirm the purchase.
Expected Output:
The system should successfully complete the order for the logged-in user and provide an order confirmation message or email.

_Test Scenario 3: Empty Cart Checkout_
**Test Steps:**
Ensure the cart is empty (no items in the cart).
Attempt to proceed to checkout.
The system should display a warning message (e.g., "Your cart is empty. Please add items to your cart before proceeding.") and prevent further action.
The user should be redirected to the shopping page to add items to their cart.
Expected Behavior:
The checkout process should be blocked if the cart is empty, and an appropriate message should be shown.
The user should not be able to proceed with an empty cart.
Expected Output:
A clear message like "Your cart is empty. Please add items to your cart before proceeding" is displayed.

_Test Scenario 4: No Payment Method Entered_
**Test Steps:**
Add items to the shopping cart and proceed to checkout as either a guest or logged-in user.
The user should be prompted to select or enter a payment method (e.g., credit card, PayPal).
If the user does not provide any payment method and tries to confirm the checkout, the system should display a warning message (e.g., "Please provide a payment method before completing your order").
Expected Behavior:
The system should require a valid payment method before allowing the user to complete the purchase.
The user should be prompted again to enter the payment information if none is provided.
Expected Output:
The system prompts for payment details if none are provided and blocks the checkout until a valid payment method is entered.

_Test Scenario 5: Returning to Cart After Checkout_
**Test Steps:**
Add items to the shopping cart and proceed to checkout as either a guest or logged-in user.
After reaching the final step of checkout (order confirmation), the user may decide to return to the cart to modify their order (e.g., remove an item).
The system should allow the user to go back to the cart and make changes before completing the order.
Expected Behavior:
The user should be able to return to the cart and modify the order before finalizing the purchase.
The checkout process should be non-disruptive, allowing users to edit items in the cart before proceeding.
Expected Output:
The cart updates appropriately, and the user can modify their order before completing the purchase.

_Test Behavior Missing in the Prompt:_
Handling of Invalid Shipping or Billing Information: The system should validate user inputs for shipping and payment details (e.g., missing address, invalid credit card number) and provide appropriate error messages.
User Session Timeout: If a logged-in user remains idle for a certain period, the system should time out and prompt the user to log in again before proceeding to checkout.
Outcome:
The test will pass if the system behaves as described in each scenario.
The test will fail if any of the expected behaviors are not met (e.g., if the cart allows checkout when empty, or if the system doesn't allow modifying the cart before finalizing the order).
