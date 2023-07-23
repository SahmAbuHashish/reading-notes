# Reading Questions

### What is React Context, and how does it help in managing state and data sharing in a React application?

React context allows us to pass down and use (consume) data in whatever component we need in our React app without using props.
In other words, React context allows us to share data (state) across our components more easily.

React Context is useful when multiple components need access to the same data or state without passing it down through all intermediate components as props. It simplifies data sharing and management and reduces the complexity of prop drilling in large applications.

---

### Explain the useContext Hook and how it can be used to access data from a React Context within a functional component.

The useContext hook is a built-in React hook that allows functional components to consume data from a React Context. It simplifies accessing context data without the need to use a Context.The useContext hook takes a context object created by React.createContext and returns the current context value provided by the nearest Context.

Instead of using render props, we can pass the entire context object to React.useContext() to consume context at the top of our component.

---

### Describe the purpose of Next.js, and provide an example from the Vercel Next.js Examples reading on how it can be used to build a scalable web application.

Next.js is a popular React framework that provides a comprehensive set of tools and features for building server-rendered React applications. Its main purpose is to simplify and streamline the development of scalable web applications by offering built-in solutions for server-side rendering, static site generation, routing, code splitting, and more.
