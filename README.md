# useEffect Runs After Every Render in React 19

This repository demonstrates an uncommon bug encountered in React 19 where the `useEffect` hook runs after every render, even when a dependency array is provided.  The unexpected behavior impacts application performance and can lead to difficult-to-debug issues.

The `bug.js` file shows the buggy implementation.  The `bugSolution.js` file provides a corrected version that addresses this issue, highlighting the correct use of `useEffect` dependencies.

## How to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `npm start`.
5. Observe the console output and the component's behavior to see the unexpected re-renders.

## Solution

The solution involves correctly specifying the dependencies in the `useEffect` hook's dependency array.  If you don't need the effect to run on every render, include only the relevant state variables or props that trigger a necessary update.  Incorrectly defining or omitting dependencies is a common source of issues with React's `useEffect`. 