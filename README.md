# Unnecessary Re-renders in React's useEffect Hook

This example demonstrates a common issue in React applications where the `useEffect` hook causes unnecessary re-renders.  The provided `MyComponent` function uses `useEffect` to log the current value of `count` to the console. However, the `useEffect` is called on every render of `MyComponent`, regardless of whether the `count` has actually changed. This can lead to performance problems, especially in complex components.

## Solution

To fix this, we should add the `count` variable to the dependency array passed to the `useEffect` hook. This ensures that the effect only runs when the value of `count` changes.

The solution file provides the corrected code.