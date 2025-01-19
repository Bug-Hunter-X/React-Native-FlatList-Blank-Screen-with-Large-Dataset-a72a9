# React Native FlatList Blank Screen Issue

This repository demonstrates a common issue encountered when using FlatList in React Native with a large dataset. The problem manifests as a blank screen, seemingly unresponsive. This happens due to the initial render blocking the main thread, leading to performance issues.

## Problem Description

The provided `bug.js` file shows a basic implementation of FlatList using a dataset of 100 items.  While this isn't excessively large, increasing the data count to several hundred or thousand will cause the app to freeze and render a blank screen.

## Solution

The solution, implemented in `bugSolution.js`, addresses this by using `windowSize` and `removeClippedSubviews` properties of `FlatList`. These are explained in the file. A better approach might involve pagination or virtualization of the dataset depending on scale, but this solution is effective for medium size datasets.