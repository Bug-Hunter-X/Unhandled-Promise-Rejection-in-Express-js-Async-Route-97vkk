# Unhandled Promise Rejection in Express.js Async Route

This repository demonstrates a common error in Node.js Express.js applications: unhandled promise rejections.  When asynchronous operations within routes throw errors, and these errors aren't properly caught, they can lead to application crashes and unpredictable behavior, particularly in production. 

**bug.js** contains the problematic code.  **bugSolution.js** provides the corrected version with robust error handling.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install express`
4. Run `node bug.js`
5. Observe the unhandled promise rejection error in the console.  The server might crash or behave erratically. 
6. Now run `node bugSolution.js` and notice the more graceful error handling. The server will respond with a 500 status code and an error message, preventing a crash.

## Solution

The solution involves using try...catch blocks within async functions to handle potential errors synchronously and comprehensively handle rejections in promises.