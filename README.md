# Uncontrolled useEffect causing infinite rerenders in React

This repository demonstrates a common React bug involving the `useEffect` hook.  An infinite loop occurs when the `useEffect` hook doesn't specify a dependency array or includes dependencies that change on every render, causing the effect to run repeatedly and trigger more renders.

## Bug Description
The provided `MyComponent` uses `useEffect` without specifying the dependencies.  This causes the effect to execute on every render, logging 'Effect runs!' to the console infinitely, triggering performance issues and potential crashes. 

## Solution
The solution involves adding an empty dependency array `[]` to the `useEffect` hook to limit it to run only once after the initial render. 