# Firebase Authentication Unsubscribe Issue

This repository demonstrates a common issue in Firebase applications: forgetting to unsubscribe from `onAuthStateChanged`.  This can lead to memory leaks and unexpected behavior, especially in React components.

The `firebaseAuthBug.js` file shows the incorrect implementation, while `firebaseAuthSolution.js` provides the corrected version with proper unsubscription.

## How to Reproduce the Bug
1. Clone this repository.
2. Set up a Firebase project and initialize Firebase in your application.
3. Run `firebaseAuthBug.js`.  Observe potential memory leak and unexpected behavior (if applicable)
4. Run `firebaseAuthSolution.js` and compare the results. 

## Solution
Always unsubscribe from Firebase listeners using the returned unsubscribe function when the component unmounts or the listener is no longer needed.