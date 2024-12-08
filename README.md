# React useEffect Warning: Unmounted Component State Update

This repository demonstrates a common React issue: receiving a warning about updating state on an unmounted component within a `useEffect` hook.

The `bug.js` file contains the problematic code. The `bugSolution.js` file shows how to resolve the issue by using a cleanup function within the `useEffect` hook.  The warning arises because asynchronous operations triggered within `useEffect` might continue after the component has been unmounted.  This can result in an error attempting to update state on a component that no longer exists in the DOM.