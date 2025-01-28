# React SetInterval Memory Leak

This repository demonstrates a common mistake in React applications involving the use of `setInterval` within the `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior.

## Problem
The `bug.js` file shows a React component that uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, resulting in a memory leak.

## Solution
The `bugSolution.js` file demonstrates the correct way to use `setInterval` in `useEffect`, including the necessary cleanup with `clearInterval`.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the counter incrementing in the browser.
5. Try to unmount the component. The interval will still continue to run even after the component is unmounted.
This is a common mistake in React. Always make sure you clean up any timers or intervals when the component is unmounted.