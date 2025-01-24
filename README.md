# Infinite Rendering Bug in React useEffect

This repository demonstrates a common bug in React applications where the `useEffect` hook causes infinite re-renders.  The bug arises from a missing dependency in the `useEffect` hook's dependency array.

## Bug Description
The `MyComponent` renders infinitely because the `useEffect` hook is missing the `count` variable in its dependency array. The `useEffect` hook runs after every render because it lacks the dependency, causing a loop of re-renders, resulting in an infinite loop.

## Bug Reproduction
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite rendering in your browser's console.

## Solution
The solution involves adding the `count` variable to the dependency array of the `useEffect` hook.