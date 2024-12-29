# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without checking for potential errors. This can result in unexpected behavior if the `id` parameter is not a valid integer.

## Bug

The provided `bug.js` file contains an Express.js route handler that is vulnerable to errors caused by invalid user IDs. The code fails to handle cases where the `userId` parameter cannot be parsed as an integer, leading to potential crashes or unexpected behavior. 

## Solution

The `bugSolution.js` file demonstrates how to fix the bug by adding proper error handling.  It includes checks to ensure that the `userId` parameter is a valid integer before attempting to use it to find a user.