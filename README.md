# Expo CLI Android Build Error: Manifest Mismatch

This repository demonstrates a bug encountered while building an Expo project for Android. The build process fails with a vague 'manifest mismatch' error, preventing the app from running on Android devices. The app functions correctly on iOS simulators. 

## Issue Description

The project, when built for Android, produces a cryptic 'manifest mismatch' error within the Expo CLI.  The error message lacks specifics about which manifest files are conflicting and does not provide clear guidance for troubleshooting.  This makes identifying and resolving the issue very challenging.   The issue has been observed using several libraries, potentially indicating a conflict stemming from dependency management or interactions between these libraries and Expo's build process.

## Steps to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` or `yarn install` to install the necessary dependencies.
4. Attempt to build the app for Android using `expo build:android`.
5. Observe the 'manifest mismatch' error.

## Solution

The solution involves carefully examining the Android manifest file (`AndroidManifest.xml`) and ensuring consistency with the app's configuration and dependencies. In this case, a specific conflict was identified with how react-native-maps was set up, and adjusting that resolved the issue.  This solution will help others to easily debug similar issues.  For detailed steps, refer to the `bugSolution.js` file.  The bug file demonstrates code that generates the mismatch error and the solution file contains corrected code. 