# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the provided code lacks handling for cases where the user ID is not a valid integer, leading to potential crashes or unexpected behavior.

## Bug

The `bug.js` file contains an Express.js route handler that fetches a user based on their ID.  However, it fails to handle situations where the `userId` parameter is not a valid integer.  This can occur if the user provides non-numeric input, resulting in `parseInt(userId)` returning `NaN`, and potentially causing an error during the array lookup.

## Solution

The `bugSolution.js` file provides a corrected version of the route handler.  It includes error handling to check if `parseInt(userId)` successfully parses to a number and returns an appropriate error response if not.