# Unintended Single Execution of useEffect with Empty Dependency Array

This repository demonstrates a common React bug involving the `useEffect` hook and its dependency array.  The provided `MyComponent` intends to log the current count every time it updates. However, due to an empty dependency array `[]`, the `useEffect` only runs once after the initial render, causing unexpected behavior.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected implementation.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output.  You'll see that the count is only logged once even though the button increments the count.

## Solution

The solution involves adding `count` to the dependency array. This ensures the effect re-runs whenever the `count` value changes.