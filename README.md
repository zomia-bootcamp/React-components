# React Components

## What Is React.js?

React is an open-source JavaScript library for building user interfaces. It was developed by Facebook and has gained significant popularity and adoption in the web development community. React allows developers to create reusable UI components and build dynamic and interactive user interfaces efficiently.

## The Benefits of Using React.js

- **Ease of Use**: React offers an easy-to-use framework for building user interfaces.
- **Seamless Update**: React's Virtual DOM and efficient diffing algorithm enable seamless updates by calculating and applying minimal changes to the real DOM.
- **Developer Tools**: React provides powerful developer tools, such as React DevTools, which allow you to inspect and debug React components efficiently.
- **The Virtual DOM**: React uses the Virtual DOM, a lightweight representation of the actual browser DOM, which enables efficient rendering and updates.
- **Reusable Components**: React promotes the creation of reusable components, allowing you to build modular and maintainable UIs.
- **Open Source**: React is an open-source library, which means it has an active community, extensive documentation, and a large ecosystem of libraries and resources to support developers.


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

In a typical React application, the export/import process allows you to share code and components between different files. Let's explain the export/import process between `App.js` and `index.js`:

1. **Exporting a Component**: In `App.js`, you define a React component, typically as a class or a function. To make this component available for use in other files, you export it using the `export` keyword. For example:

```jsx
// App.js
import React from 'react';
import NewComponent from './NewComponent';

const App = () => {
  return (
    <div>
      {/* Existing code */}
      <NewComponent />
    </div>
  );
};

export default App;

```

In this example, the `App` component is exported as the default export using `export default App;`.

2. **Importing a Component**: In `index.js` or any other file where you want to use the exported component, you import it using the `import` statement. The import statement allows you to bring in the exported component and use it within the file. For example:

```jsx
// index.js
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(<App />, document.getElementById('root'));
```

In this example, the `App` component is imported using `import App from './App';`. Now, you can use the `App` component within the `index.js` file.


In a React application, you need to import components into App.js (or any other file) to use them because components are the building blocks of your user interface.

In React, you build your user interface by composing smaller, reusable components. By importing components into App.js, you can use them within the App component's JSX to define the structure and layout of your application. This allows you to create complex UIs by combining different components together.

### Exercises

Import your `FirstComponent` into `App.js` based on the existing process, you can follow these steps:

1. Export your component at the bottom of your `FirstComponent` file:

```jsx
// FirstComponent.js
import React from 'react';

const FirstComponent = () => {
  // Component code here
  return <div>New Component</div>;
};

export default FirstComponent;
```

2. In `App.js`, you can import the `FirstComponent` component and use it within the `App` component:

```jsx
// App.js
import React from 'react';
import FirstComponent from './FirstComponent';

class App extends React.Component {
  render() {
    return (
      <div>
        {/* Existing code */}
        <FirstComponent />
      </div>
    );
  }
}

export default App;
```

By importing the `FirstComponent` and including it within the `App` component's JSX, you can now use the new component within `App.js`.

Remember to ensure that the file paths are correct and relative to the file you are importing from.







