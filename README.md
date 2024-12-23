# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to a missing dependency in the `useEffect` call. 

## Bug Description

The `MyComponent` function uses `useState` and `useEffect` to update a counter.  However, the `useEffect` hook lacks the `count` variable in its dependency array. This means the effect runs after every render, causing the `count` to update, triggering another render, and resulting in an infinite loop.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the browser's console and the rapidly increasing counter.