# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by incorrectly using the `useEffect` hook.  The `useEffect` hook attempts to update the `count` state within its dependency array, causing a continuous re-render and an infinite loop.  The solution demonstrates how to correctly use the `useEffect` hook to avoid this issue.

## Bug
The `bug.js` file contains the buggy code.  The `useEffect` hook, without any dependencies, sets a new state based on the previous state causing an infinite render loop.

## Solution
The `bugSolution.js` file provides a corrected version.  This revised code uses `count` as a dependency in the `useEffect` hook. It only runs when the `count` value changes which means that useEffect will only run once. The useEffect will no longer cause an infinite loop.