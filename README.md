# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite loop. The component renders repeatedly, resulting in excessive console logging and potential performance issues.

## Bug Description
The `useEffect` hook, without a dependency array, runs after every render.  In this case, it logs the current count to the console.  Because updating the count triggers a re-render,  which in turn triggers `useEffect` again, creating an infinite loop.  

## Solution
The solution is to add a dependency array to the useEffect hook.  This array specifies the variables the effect depends on. The effect only runs if any of these variables change.

## How to Reproduce
1. Clone this repo.
2. Run `npm install`
3. Run `npm start`

Observe the infinite logging in the console.