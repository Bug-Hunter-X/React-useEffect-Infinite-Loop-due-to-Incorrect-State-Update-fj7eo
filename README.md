# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook and incorrect state updates. The bug leads to an infinite loop, causing the application to crash or become unresponsive.

## Bug Description
The `MyComponent` function uses the `useState` hook to manage a counter.  The `useEffect` hook attempts to update the state directly within the function, resulting in an infinite re-render cycle.  This occurs because every change to the state triggers a re-render, leading to repeated calls to the `useEffect` hook, and repeated updates to the state, creating a loop.

## Solution
The solution involves correctly updating the state using the functional update pattern with `useState`. This ensures that the state updates are based on the previous state value and prevent the infinite loop.

## How to reproduce
Clone the repository and run `npm install`. Then, run `npm start`. You will observe the infinite loop and consequent errors in the browser's console.

## How to fix
Refer to the `bugSolution.js` file for the corrected code.