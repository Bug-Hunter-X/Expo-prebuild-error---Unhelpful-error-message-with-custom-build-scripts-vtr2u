# Expo prebuild error: Unhelpful error message with custom build scripts

This repository demonstrates a bug in Expo's `expo prebuild` command when used with a project containing custom build scripts. The error message produced is unhelpful, making debugging difficult.

## Problem

When running `expo prebuild`, the build process fails due to a conflict between Expo's internal build steps and a custom script that modifies files.  The error message does not clearly indicate the source of the problem, hindering effective troubleshooting.

## Solution

The solution involves carefully reviewing the custom build script to ensure it doesn't interfere with the files Expo expects to find during the prebuild process.  Potential issues involve modifications to the files' structure, content, or existence.

## Reproduction

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run `expo prebuild` and observe the unhelpful error message.
4. Examine the `bugSolution.js` file for a solution that avoids the conflict.