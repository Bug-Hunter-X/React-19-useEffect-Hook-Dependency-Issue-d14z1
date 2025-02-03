# React 19 useEffect Hook Dependency Issue

This repository demonstrates a common error when using the `useEffect` hook in React 19: forgetting to include all relevant state variables in the dependency array.

## The Bug
The `bug.js` file contains a functional component that increments a counter.  The `useEffect` hook logs the current count to the console. However, if the dependency array is missing `count`, the effect will only run once on mount. This can lead to unexpected behavior and debugging challenges.

## The Solution
The `bugSolution.js` file shows the corrected code. By including `count` in the dependency array, the `useEffect` hook now runs whenever the `count` state variable changes, logging the correct value each time.

## How to reproduce
1. Clone this repository.
2. Navigate to the repository directory in your terminal.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server.
5. Open your browser and observe the console logs.