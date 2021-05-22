# Redux - Combined Reducers

## Review, Research, and Discussion

1. **Why choose Redux instead of the Context API for global state?**

In a large scale application, Redux is a better way to control state.

2. **What is the purpose of a reducer?**

Buffer that sits and protects the application state, changes to state by the components have to be passed through the reducer and have to play by the reducers rules. Reducer is a function that runs every time state needs to be updated, and always returns the new state of the application.

3. **What does an action contain?**

Object literals that tell the reducer what is being done to the app, and any data required for the update.

4. **Why do we need to copy the state in a reducer?**

Reducers are not allowed to modify the existing state, instead they must make immutable updates by copying the existing state and making changes to the copied values. (source: Redux [docs](https://redux.js.org/tutorials/fundamentals/part-3-state-actions-reducers))

## Vocabulary Terms

- **Immutable state**: State cannot be modified, reducers must make copies of existing state to make updates.
- **Time travel in Redux**: Redux DevTools records dispatched actions and the state of the Redux store at every point in time, which makes it possible to inspect the state and travel back in time to a previous application state without reloading the page or re-starting the app. (source: [Medium - Redux DevTools](https://medium.com/the-web-tub/time-travel-in-react-redux-apps-using-the-redux-devtools-5e94eba5e7c0))
- **Action Creator**: Instead of creating action objects inline in the places where you dispatch actions, can create functions generating them. You might write an action creator into a separate file, and import it into your component. (source: [Redux docs](https://redux.js.org/recipes/reducing-boilerplate))
- **Reducer**: Functions that take current state and an action as arguments, and return a new state result, (state, action) => newState. (source: Redux docs [writing reducers](https://redux.js.org/tutorials/fundamentals/part-3-state-actions-reducers))
- **Dispatch**: A store holds the whole state tree of the application, the only way to change the state inside it is to dispatch an action on it. (source: Redux docs [store](https://redux.js.org/api/store))

## Preparation Materials

### [Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)
- `import {combineReducers, createStore } from 'redux';`
- Example reducer: `const userReducer = (state={}, action) => { return state };`
- Example combineReducer example: `const reducers = combineReducers({user: userReducer, tweets: tweetReducer})`

### [Redux Docs: Using Combined Reducers](https://redux.js.org/recipes/structuring-reducers/using-combinereducers/)
- Takes an object of reducer functions and returns a new reducer function
- `createStore` function takes `preloadedState` as a second argument

### [Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/)
- Reducers passed to `combineReducers` must satisfy the following:
   - any action that is not recognized, must return state that was given as first argument
   - must never return undefined
   - if `state` given to it is undefined, must return initial state for the specific reducer