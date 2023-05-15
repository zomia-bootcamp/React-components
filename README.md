## React Components

## What is a component?

A React component is like a building block or a puzzle piece that helps create the user interface of a web application. It represents a specific part or functionality of the application.

![component diagram](https://miro.medium.com/v2/resize:fit:1400/1*NX0GtVytAI8soIUMAuUSeQ.png)

By combining multiple components together, you can create a complete user interface for your web application. Each component focuses on a specific task, and they work together to build a cohesive and interactive experience for the users.

Let's head over to the [Airbnb](https://www.airbnb.com/) website, and see how components are used in the real world.

## Creating a Function Component

In React, we can define components using JavaScript functions. This type of component is called a function component. Function components have become the standard in modern React applications, especially with the introduction of Hooks.

Function components allow us to break down our interface into smaller, reusable pieces. We can create components for specific parts of our website, such as the search bar, navigation bar, or dashboard content. These components can be easily composed to build complex React applications.

Let's take a closer look at an example from the previous exercise:

```jsx
import React from 'react';

function MyComponent() {
  return <h1>Hello, I'm a functional React Component!</h1>;
}

export default MyComponent;
```

In this code snippet, we define a function component called `MyComponent`. Inside the function, we use the `return` statement to specify the JSX code that represents the component's output. In this case, it's a simple `<h1>` element with a greeting.

The `export default` statement allows us to export `MyComponent` so that it can be used in other parts of our application.

By using function components, we can create reusable and modular code, making our React application more maintainable and easier to understand. As we progress, we will explore more advanced techniques and patterns to build powerful React components.

### Exercises

In the root directory of this project, create a new directory called `components`, with a new file called `FirstComponent.js`.
Import the React library at the top of the file, and declare a new function component. You can call this whatever you’d like.

## Name a Functional Component

When you create a new functional component, you need to give it a name. In our example, we named our component "MyComponent":

```jsx
function MyComponent() {
  return <h1>Hello world</h1>;
}
```

It's important to follow a naming convention for function components. The name should start with a **capital letter** and use **PascalCase**. This convention is specific to React. By capitalizing the name, React understands that it's a component and not an HTML tag.

This is a specific rule in React. If you're creating a component, remember to start its name with a capital letter. If you use a lowercase letter, React will mistake it for a built-in component like `div` or `input`, and it will cause an error.

### Exercises

Navigate to [FirstComponent.js](./components/FirstComponent.js), and verify that your component name meets the react namig convention.
If not, correct it.

















React applications are composed of components, which are small, reusable chunks of code responsible for specific tasks. One common task is rendering HTML and updating it when data changes.

Let's take a closer look at the code provided:

```jsx
import React from 'react';
import ReactDOM from 'react-dom/client';

function MyComponent() {
  return <h1>Hello world</h1>;
}

ReactDOM.createRoot(
  document.getElementById('app')
).render(<MyComponent />);
```

In the code snippet above, we have several unfamiliar elements, but don't worry. We will break it down step by step.

- The `import` statements bring in the necessary dependencies, including `React` and `ReactDOM`.
- The `function MyComponent()` defines a custom React component called `MyComponent`. It returns JSX code that renders an `<h1>` element with the text "Hello world".
- `ReactDOM.createRoot()` creates a React root to render our component. The `document.getElementById('app')` specifies the target element where the component will be rendered.
- The `render()` method is called on the created root, with `<MyComponent />` as the JSX content to be rendered.

By understanding the structure and purpose of React components, you are on your way to building dynamic and interactive user interfaces using React.
