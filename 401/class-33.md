# Context API

## Review, Research, and Discussion

1. **Describe use cases for useMemo() and useReducer()**

useReducer can be used for complex data objects that you need to update different properties within. [src](https://medium.com/@binyamin/react-hooks-usereducer-usecallback-usememo-5e5af9b0257a)
useMemo memoizes a value, saving it to the cache and not running it again during re-renders unless the value changes.

2. **Why do custom hooks need the use prefix?**

It's a convention, and without it react wouldn't be able to automatically check for violations of rules of hooks. [src](https://stackoverflow.com/questions/59809947/why-are-react-hooks-named-in-this-fashion-usexxx)

3. **What do custom hooks usually do?**

extract component logic into reusable functions [src](https://reactjs.org/docs/hooks-custom.html)

4. **Using any list of custom hooks, research and name one that you think will be useful in your applications**

useWebSocket would be useful when building a game web app that needs to communicate with a websocket api. [src](https://medium.com/javascript-in-plain-english/useful-custom-hooks-for-tired-react-devs-f2f602dc754f)

5. **Describe how a hook that fetches API data might work.**

We could abstract the logic for fetching the data into a custom hook then call that in useEffect for example on multiple pages if they all need access to data from that api call [src](https://medium.com/better-programming/how-to-fetch-data-from-an-api-with-react-hooks-9e7202b8afcd)

## Vocabulary Terms

- **reducer:** A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. [src 1](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/#:~:text=A%20reducer%20is%20a%20function,so%20that%20they%20behave%20consistently.) [src 2](https://www.robinwieruch.de/javascript-reducer)

## Context API

Context provides a way to pass data through the component tree without having to pass props down manually at every level.

When to Use Context Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. For example, in the code below we manually thread through a “theme” prop in order to style the Button component:

Using context, we can avoid passing props through intermediate elements:

Before You Use Context Context is primarily used when some data needs to be accessible by many components at different nesting levels. Apply it sparingly because it makes component reuse more difficult.

If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.

## Preparation Materials

* [context api](https://reactjs.org/docs/context.html)
* [hooks and context example](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b)
* [react context links](https://github.com/diegohaz/awesome-react-context)
