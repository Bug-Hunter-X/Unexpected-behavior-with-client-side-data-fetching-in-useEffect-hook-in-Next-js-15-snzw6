# Unexpected behavior with client-side data fetching in useEffect hook in Next.js 15

This repository demonstrates an unexpected behavior encountered when using client-side data fetching within the useEffect hook in a Next.js 15 application.

## Bug Description

A simple counter is implemented on the About page using the useState and useEffect hooks.  The counter is expected to increment every second. However, the counter increments rapidly and unexpectedly, not stopping as intended.

## Setup

1.  Clone the repository.
2.  Navigate to the project directory.
3.  Run `npm install` to install dependencies.
4.  Run `npm run dev` to start the development server.

## Reproduction

Visit the `/about` page in the browser.  Observe the counter behavior.  The counter increments at a much faster rate than one second intervals.

## Solution

The provided solution addresses the issue by using the `useRef` hook.  This ensures that the interval is cleared only when the component is unmounted, correctly solving the counter's rapid incrementing.