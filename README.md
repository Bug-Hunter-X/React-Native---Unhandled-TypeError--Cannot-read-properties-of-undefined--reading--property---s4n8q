# React Native: Handling Null or Undefined Property Access

This repository demonstrates a common error in React Native applications: attempting to access a property of an object that is currently null or undefined. This usually happens when dealing with asynchronous data fetching or before a component fully mounts.

The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The main issue lies in accessing a property (`data.name` in this example) before ensuring that `data` has been properly fetched and assigned a value.  This frequently results in a runtime error like `TypeError: Cannot read properties of undefined (reading 'property')`.

## Solution

The solution involves adding checks to handle the cases where `data` might be null or undefined before accessing its properties.  Optional chaining (`?.`) and nullish coalescing (`??`) are effective approaches.