# Express.js Route Handler Missing Return Statement

This repository demonstrates a common error in Express.js route handlers: missing `return` statements in conditional branches.  This can lead to unexpected behavior and multiple responses being sent.

## Bug
The `bug.js` file contains an Express.js route handler that fetches user data. If the user is not found, it sends a 404 response. However, it's missing a `return` statement before `res.status(404).send()`, which causes the code to continue executing and potentially send another response.

## Solution
The `bugSolution.js` file provides the corrected code with the missing `return` statement added, preventing this issue.

## How to reproduce
1. Clone this repository
2. Run `npm install`
3. Run `node bug.js` and make a request to a non-existent user ID. Observe the unexpected behavior.
4. Run `node bugSolution.js` and make the same request. Observe the correct behavior.