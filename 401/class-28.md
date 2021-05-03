# Component Composition

## Review, Research, and Discussion

1. **Can a parent component access the state of a child component?**

Can access the child's state using Refs. Assign Refs for the child component in the parent component, then using Refs can access the child's state. Refs are created using React.createRef() and attached to React elements via the ref attribute. (source: [GeeksforGeeks](https://www.geeksforgeeks.org/how-to-access-childs-state-in-react/))

2. **What can be passed along in a prop variable?**

Any information, function, JavaScript that needs to be passed down.

3. **How can a child component “know” the state of another component?**

To obtain the state of another component, you can pass the component's state to it's child components as props. You can also have components share a common ancestor, and have them access the same state in a similar manner. (source: [codecademy](https://discuss.codecademy.com/t/can-a-component-access-the-state-of-another-component/394157))

## Vocabulary Terms

- **Component Props**: Keyword in React for properties, can be any information, function, JavaScript that needs to be passed to another component. Can only be passed in one direction, from the root to its children, no way for data to be passed up.

- **Component State**: React components have built in state object, which is where you story property values that belong to the component. When the state object changes, t he component re-renders. (source: [W3Schools](https://www.w3schools.com/react/react_state.asp))

- **Application State**: In an application, state is interface between data (from backend or local change) and the representation of this data with UI elements on the front-end. State is able to keep the data of different components in sync because each state update will rerender all relevant components. State can be a medium to communicate between different components as well. (source: [Medium - DailyJS](https://medium.com/dailyjs/comparison-of-state-management-solutions-for-react-2161a0b4af7b))
