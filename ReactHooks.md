# Hook:

*⇒ Hooks* are special functions that are only available while React is [rendering](https://react.dev/learn/render-and-commit#step-1-trigger-a-render) 


# useState():

⇒ The `useState` hook is a fundamental React hook that allows you to add state management to functional components. 

⇒ It enables you to create state variables and update their values within a functional component.

⇒ `useState` is a React Hook that lets you add a [state variable](https://react.dev/learn/state-a-components-memory) to your component.

⇒ Syntax:   
      `const [state, setState] = useState(initialState)`

⇒ `useState` takes an initial state value and returns an array with two items:

                                     1. The current state value.

                                     2. A function to update the state.

⇒ Updating the state using the provided function triggers a re-render of the component, reflecting the new state.

⇒ It is primarily used for managing local component state in functional components.


# useEffect():

⇒ The `useEffect` hook allow you to perform side effects in your components.

⇒ `useEffect` is a React Hook that lets you [synchronize a component with an external system.](https://react.dev/learn/synchronizing-with-effects)

⇒  `useEffect` accepts two arguments:

                  1. A function that contains the side effect logic.

                       2. An optional dependency array that determines when the effect should re-render.

⇒ Dependency Array: (important)
    - If the dependency array is empty (`[]`), the effect runs only once, after the initial render.

    - If the dependency array contains specific state or props, the effect will run after every render where those dependencies change.

    - If no dependency array is provided, the effect runs after every render, potentially causing performance issues.

⇒ Syntax:
           `useEffect( setup(basically a callback function), dependencies?(basically a array) )` 

           `useEffect( () => {} , [] )`

⇒ `useEffect` is a versatile hook for handling side effects in React and is essential for making,

           → API calls like fetching data from api

           → Directly updating the DOM

           → Timers like SetTimeOut and SetInterval


# useRef():

⇒ `useRef`  is a react hook that allow us to create a mutable variable, which will not re-render the component.

⇒ `useRef`  is also used for accessing the DOM element.

⇒ `useRef` returns a mutable object with a `.current` property.

⇒ Changes to the `.current` property do not cause re-renders of the component.

⇒ The `.current` property can be initialized with a value (e.g., `useRef(initialValue)`) or left as `null` (e.g., `useRef(null)`).

⇒ Syntax:
              `const ref = useRef(initialValue)`

⇒ `useRef` is often used for:
    
    → Accessing and interacting with DOM elements directly (e.g., focusing an input field).
    
    → Changing it does not trigger a re-render (unlike state variables, which trigger a re-render).
    
    → You can store information between re-renders (unlike regular variables, which reset on every render).
    

⇒ Unlike `useState`, updating the value of `useRef` does not trigger a component re-render.

⇒ Changing a ref does not trigger a re-render, so refs are not appropriate for storing information you want to display on the screen. Use state for that instead. Read more about [choosing between `useRef` and `useState`.](https://react.dev/learn/referencing-values-with-refs#differences-between-refs-and-state)

⇒ The `useRef` hook is a versatile tool in React, useful for direct DOM manipulation and storing mutable values that do not require a component re-render when updated.