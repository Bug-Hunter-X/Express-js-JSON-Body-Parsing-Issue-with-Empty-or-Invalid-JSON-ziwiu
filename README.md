# Express.js JSON Body Parsing Issue

This repository demonstrates a common issue encountered when parsing JSON request bodies in Express.js applications. The problem arises when the request body is empty or contains invalid JSON data, leading to unexpected behavior or errors.

## Bug Description

The Express.js application fails to parse JSON request bodies correctly when the request body is empty or when it contains malformed JSON data. This can manifest as an empty `req.body` object or an unexpected error.

## Solution

The solution involves adding middleware to handle cases where the request body is empty or contains invalid JSON data gracefully.

## How to reproduce

1. Clone this repository
2. Navigate to the root folder
3. run `npm install`
4. run `node bug.js`
5. Send an empty JSON request to `/data` endpoint using a tool like Postman.
6. Observe the console log which shows that the request body is empty.
7. Send an invalid JSON request such as `{"key": value}` to `/data` endpoint.
8. Observe the error in the console.

## Solution

The solution is implemented in `bugSolution.js`. It uses a middleware function to check for empty or invalid JSON before proceeding.