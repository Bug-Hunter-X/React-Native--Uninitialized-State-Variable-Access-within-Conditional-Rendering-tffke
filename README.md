# React Native: Uninitialized State Variable Access

This repository demonstrates a common error in React Native: accessing a state variable before it's initialized, often within a conditional statement or before component mount.  The error manifests as undefined behavior or crashes. The solution shows how to correctly handle state initialization and conditional rendering to prevent this issue.

## Problem

The `bug.js` file showcases the problematic code.  Attempting to access the `count` state variable within the `if` condition before React has had a chance to initialize it leads to `count` being `undefined`.

## Solution

The `bugSolution.js` file presents the corrected code.  It uses the optional chaining operator (`?.`) to safely access `count`, handling the case where it might still be `undefined`.  Alternatively, you could refactor the conditional logic or use a default value when initializing the state.

## How to run

1. Clone this repository.
2. Navigate to the project directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `npx react-native run-android` or `npx react-native run-ios` to run the app on your device or emulator.

Observe the console logs and the application's behavior in both the original problematic code and the corrected solution.