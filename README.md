# React Native Crash: Third-Party Library Asynchronous Issue

This repository demonstrates a common error in React Native development involving crashes or unexpected behavior due to improper asynchronous handling in third-party libraries.  The issue typically arises when a library attempts to directly update the UI from a background thread.  This often manifests as seemingly random crashes or inconsistent behavior.

## Bug Description
The bug is caused by the `BuggyThirdParty` library, which attempts to update the UI state asynchronously without using proper mechanisms such as `setTimeout` or `setImmediate`. This leads to unpredictable behavior and potential crashes.

## Solution
The `FixedThirdParty` library demonstrates the correct approach using `setImmediate` to ensure UI updates happen on the main thread, preventing crashes and ensuring consistent behavior. 