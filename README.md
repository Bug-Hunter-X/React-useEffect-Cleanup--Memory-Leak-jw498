# React useEffect Cleanup: Memory Leak

This example demonstrates a common mistake in React's `useEffect` hook: forgetting to properly clean up resources (like intervals, timeouts, event listeners, etc.) when a component unmounts.  Failing to do so can lead to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains a component that uses `useEffect` to update a counter every second. However, it's missing the return statement in `useEffect` for clearing the interval.  This means that when the component is unmounted, the interval keeps running, causing a memory leak.

## Solution
The `bugSolution.js` file corrects this by adding a return statement to the `useEffect` hook. This ensures that the interval is cleared when the component is unmounted, preventing the memory leak.