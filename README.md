# React setInterval Memory Leak
This repository demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook: forgetting to return a cleanup function.  This can lead to memory leaks as the interval continues to run even after the component unmounts.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it lacks the cleanup function required to stop the interval when the component is unmounted, resulting in a memory leak.

## Solution
The `bugSolution.js` file provides the corrected implementation, where a cleanup function is returned from the `useEffect` hook. This function clears the interval when the component is unmounted, preventing the memory leak.

## How to Reproduce
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the behavior of both `bug.js` and `bugSolution.js`.