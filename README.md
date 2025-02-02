# Unhandled Promise Rejection in React Native Async Operation

This repository demonstrates a common React Native bug: attempting to access component state before it has finished mounting.  The bug is shown in `bug.js`, and the solution is provided in `bugSolution.js`.

## Bug Description
The component makes a network request to fetch data. The `render` method attempts to access and display this data before the `componentDidMount` lifecycle method has a chance to update the state, leading to an error, particularly if the request takes longer than the rendering process. 

## Solution
The solution utilizes the conditional rendering to avoid error in this case. We check if the data is available before attempting to render it. If it is not, it displays a loading message.