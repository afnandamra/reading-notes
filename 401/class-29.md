# Routing

## Review, Research, and Discussion

1. **Do child components have direct access to props/state from the parent?**

Child components have access to state from the parent (this.state) when in a class, and have access to props as a functional component.

2. **When a component “wraps” another component, how does the child component’s output get rendered?**

Gets rendered when there is an update to state.

3. **Can a component, such as `<Content />`, which is a child also be used as a standalone component elsewhere in the application?**

I don't think so, standalone components have no parents to get props from or children to pass props to. (source: [Medium](https://medium.com/capgemini-web-development/integrating-stand-alone-react-components-on-a-static-page-21dd4fd3074))

4. **What trick can a parent use to share all props with it’s children**

Can pass all the props with the spread operator: `<ChildComponent {...props}>` (source: [Flavio Copes article](https://flaviocopes.com/react-pass-props-to-children/))

## Vocabulary

- **props.children**: can be used on components that represent generic boxes and don't know their children ahead of time (per React docs). It can be used to display whatever you include between the opening and closing tags when invoking a component (source: [Codeburst](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891))
- **Composition**: the act of combining parts or elements to form a whole, components are the UI building blocks in React applications like pure functions are the building blocks of function composition. (source: [Medium](https://medium.com/leanjs/react-is-all-about-composition-f9f49dec183c))
