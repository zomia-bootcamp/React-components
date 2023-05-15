# React Components

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


## The Return Keyword in Functional Components

When we create a functional component, we're basically creating a blueprint that can generate the necessary elements whenever we use its name. It generates these elements by following a set of instructions that we provide.

If you think this sounds similar to a regular JavaScript function, you're correct! Functional components can be seen as similar to regular JavaScript functions, but their purpose is to assemble a part of the user interface based on the given instructions.

Now, let's talk more about these instructions.

Firstly, the instructions should be written inside the function's curly braces. It's like a code block that contains the instructions:

```jsx
function Button() {
  // Instructions go here, inside the curly braces.
}
```

These instructions can include a combination of HTML markup, CSS, and JavaScript to create the desired outcome. However, there's one important requirement - we must always include a `return` statement.

The function is expected to generate JSX code that can be used to display something on the web browser. Therefore, when we define functional components, we need to return a JSX element.

```jsx
function BackButton() {
  return <button>Back To Home</button>;
}
```

Of course, just defining `<button>Back To Home</button>` doesn't actually display it on the browser yet. We've only defined our component.

Let's continue so we can learn how to render it and understand why the `return` statement is necessary!

### Exercises

In [FirstComponent.js](./components/FirstComponent.js), add a `return` statement with a jsx expression.


## Importing and Exporting React Components


Before we can use our defined component and render it on the web page, there are a few more steps we need to take.

In a typical React application, there are two main files: `App.js` and `index.js`. `App.js` is the top level of the application, and `index.js` is the entry point.

So far, we've defined our component inside `App.js`. However, because index.js is the entry point, we need to export our component from App.js to index.js so that it can be rendered.

React components are great because they are reusable. We can keep our component pieces separate, organized, and reusable by putting them in separate files and exporting them to where we need them.

To export a component, we can use the `export` keyword and specify whether it's a default export or a named export. In this case, we'll stick with a default export. If you need a reminder about exports, you can check out the MDN web docs.

After defining the function component in App.js, we can export it as the default export like this:

```jsx
export default MyComponent;
```

Then, we can go to our index.js file and import our component from './App':

```jsx
import MyComponent from './App';
```

This allows us to use `MyComponent` in index.js.

---

Let me know if you need any further assistance!

![exports](https://i.stack.imgur.com/uCCXS.png)














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
