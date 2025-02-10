# React useEffect Hook Misuse
This example demonstrates a common mistake when using the `useEffect` hook in React. The provided `MyComponent` intends to log a message whenever the `count` state variable updates, however, it only logs on the initial mount of the component.

## Bug Description
The issue stems from the empty dependency array `[]` in the `useEffect` hook. This causes the effect to only run once after the initial render.  The intended behavior is to log a message every time the `count` changes.

## Solution
The correct approach is to include `count` in the dependency array, so the effect runs whenever `count` updates.