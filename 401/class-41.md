# Class 41: React Native

## Review, Research, and Discussion

1. **Compare and Contrast Redux Toolkit with Redux “Ducks”**

Ducks is a way to bundle reducers, action types, and actions into the same file. Rather than splitting up related code, it can be packaged into redux modules. (source: [Medium](https://medium.com/swlh/the-good-the-bad-of-react-redux-and-why-ducks-might-be-the-solution-1567d5bdc698)) Redux Toolkit's goal is to help simplify common Redux use cases. It is not intended to be a complete solution for everything you might want to do with Redux, but it should make a lot of Redux-related code you need to write a lot simpler. Redux Toolkit exports several individual functions that you can use in your application, and adds in dependencies on some other packages that are commonly used with Redux. (source: Redux toolkit [docs](https://redux-toolkit.js.org/usage/usage-guide))

2. **What is the principle advantage of Redux Toolkit**

Helps to solve three major problems with Redux: configuring a Redux store, adding numerous packages to get Redux to things, and removing unnecessary or boilerplate code. (source: [LogRocket](https://blog.logrocket.com/smarter-redux-with-redux-toolkit/))

## Vocabulary Terms

- **Redux Toolkit slices**: Redux slice is a collection of reducer logic and actions for a single feature of application (source: [Medium](https://medium.com/swlh/redux-in-react-js-reducers-and-slices-bafafec781e3)). Redux state is typically organized into slices, defined by the reducers that are passed to combineReducers (source: Redux toolkit [docs](https://redux-toolkit.js.org/usage/usage-guide))
- **Namespace**: Programming paradigm of providing scope to identifiers (names of types, functions, variables, etc) to prevent collisions between them. JavaScript does not provide namespace by default. However, we can replicate this functionality by making a global object which can contain all functions and variables. (source: [GeeksforGeeks](https://www.geeksforgeeks.org/javascript-namespace/))

## Preparation Materials

### [getting started with react native](https://reactnative.dev/docs/getting-started)
- open source framework for building Android and iOS applications using React
- "Views" are the building blocks of iphone and android apps
- React native allows for developing "native apps" that would otherwise be written in Kotlin or Java for Android and Swift or Obective-C for iOS
- Core components, essential ready to use native components already built and available

### [react native basics (Tutorial)](https://reactnative.dev/docs/tutorial)
- `import { Text, View } from 'react-native';`
- Native components: `View`, `Text`, `Image`, `Button`, `StyleSheet`

### [react native](https://reactnative.dev/)
### [expo](https://expo.io/)
### [expo snack](https://snack.expo.io/)
### [ejecting](https://docs.expo.io/versions/latest/expokit/eject)