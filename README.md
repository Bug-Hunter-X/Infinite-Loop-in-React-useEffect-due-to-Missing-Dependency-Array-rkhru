# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The `useEffect` hook, without a dependency array, runs after every render, causing an infinite loop if it modifies state or props that trigger a re-render.  This example shows the problem and its solution.

## Bug

The `bug.js` file contains a component that uses `useEffect` without a dependency array.  This causes the `console.log` statement to execute repeatedly, leading to an infinite loop and overwhelming the console.

## Solution

The `bugSolution.js` file demonstrates the correct usage of `useEffect` by including a dependency array.  The dependency array specifies that the effect should only run when the `count` variable changes.