# Node.js Server Freeze Bug

This repository demonstrates a common Node.js issue: a server freezing due to a long-running synchronous operation within the request handler.  The `bug.js` file contains code that simulates this problem. The `bugSolution.js` file provides a solution using asynchronous programming to prevent the freeze.

## How to Reproduce

1. Clone the repository.
2. Run `node bug.js`.
3. Send a request to `http://localhost:3000`.  Notice that subsequent requests will not be processed until the first request completes.

## Solution

The solution involves refactoring the code to use asynchronous operations.  This ensures that the event loop remains responsive even while long-running tasks are in progress. See `bugSolution.js` for an example.