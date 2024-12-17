# React Router v6 Nested Route with Params Issue

This repository demonstrates a common issue encountered when using nested routes with parameters in React Router v6.  The problem occurs when a nested route is defined under a parent route that also uses parameters.  In this specific case, the `/users/:id` route fails to render correctly.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides a solution and explanation. 

## Problem Description
The nested route `/users/:id` fails to render correctly, preventing access to user details. This is despite the parent route rendering correctly and even passing parameters as intended. 

## Solution
The issue is addressed by using the `useParams` hook in the nested component to correctly access route parameters.

## How to Reproduce
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/users/1` (or any valid user ID). Observe that the User component does not render.  Navigating to `/` and `/about` works correctly, showing the home and about components.