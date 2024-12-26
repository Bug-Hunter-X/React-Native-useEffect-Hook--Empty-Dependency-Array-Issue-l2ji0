# React Native useEffect Hook: Empty Dependency Array Issue

This repository demonstrates a common issue with the `useEffect` hook in React Native when used with an empty dependency array (`[]`).  The issue is that when state or props change, even with an empty dependency array, the effect does not rerun.  This differs from web React where it normally runs only once.

## Problem
The `useEffect` hook with `[]` is intended for side effects that should only run once when the component mounts. However, in React Native, this behavior isn't consistently reliable. Changes in state or props might not trigger a re-render and re-execution of the effect. 

## Solution
Add the relevant state or prop to the dependency array. This is the more straightforward approach to fixing it, ensuring that useEffect runs whenever there's a change.