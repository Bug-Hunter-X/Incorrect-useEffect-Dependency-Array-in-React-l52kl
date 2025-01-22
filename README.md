# Incorrect useEffect Dependency Array in React

This example demonstrates a common mistake when using the `useEffect` hook in React.  The `useEffect` hook is intended to perform side effects based on changes to props or state. However, using an empty dependency array (`[]`) will cause the effect to only run once after the initial render, even if the state changes.  This can lead to unexpected behavior if the effect needs to update based on state changes.

## Bug

The `bug.js` file contains a component that attempts to log the current count to the console. However, due to the empty dependency array in `useEffect`, the console log only happens once upon initial render. Subsequent state changes via the increment button won't trigger the effect.

## Solution

The `bugSolution.js` file fixes the issue by adding `count` to the dependency array. Now, the effect will run whenever the `count` changes, providing the correct output to the console.