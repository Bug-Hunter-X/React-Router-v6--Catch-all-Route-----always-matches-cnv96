# React Router v6 Catch-all Route Issue

This repository demonstrates a common issue in React Router v6 where the catch-all route (`path="*"`) unexpectedly matches all paths, preventing other routes from working correctly. The problem arises when the catch-all route is placed without considering the order of routes or other matching conditions.  This often leads to a 404 page always being displayed.

## How to Reproduce

Clone this repo and run `npm install`. Then, run `npm start`.  You'll notice that regardless of the URL, the 404 page always renders.

## Solution

The solution involves carefully ordering routes. More specific routes should be defined *before* the catch-all route.