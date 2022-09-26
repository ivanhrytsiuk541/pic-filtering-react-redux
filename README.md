# Redux Simple Picture filtering

## Installation
```
npm install
npm start
open http://localhost:3000
```

ESLint
```
npm run lint
```

## Why do we need Redux?
Let's think about an ordinary React app. There are components, states, props and API actions. A component calls another components and if you trigger an UI state, view is updated and etc... Finally, the app becomes complex and you cannot control it.

> React is a JavaScript library for creating user interfaces by Facebook and Instagram. Many people choose to think of React as the V in MVC.
>
> Source: https://facebook.github.io/react/docs/why-react.html

We need a state container like Redux. How does Redux solve this problem?
Basically, there is a single store source which is read-only. If you want to make an action like load photos from API, you have to make this using actions and reducers.

There are 3 primary parts of Redux: actions, reducers and store.

#### Actions
Actions are used to get data. API requests can be made in this part.

> Actions are payloads of information that send data from your application to your store. They are the only source of information for the store.
>
> Source: https://redux.js.org/docs/basics/Actions.html

#### Reducers
Data comes to Reducers, and it is reshaped here. After that, it is passed to views. You can combine previous state with next state in this step.

#### Store
In the Redux, there is only one store. It can be created directly using createStore as well as applyMiddleware.

#### Calling Actions

Before call an action, we have to combine actions and dispatch function. *connect([mapStateToProps], [mapDispatchToProps], [mergeProps], [options])* function connects a React component to a Redux store.

**bindActionCreators(actionCreators, dispatch)** combines actions and dispatch function.



## Directory structure
```
Root
├── public
│   ├── actions
├── src
│   ├── actions
│   │   └──
│   ├── api
│   │   └──
│   ├── components
│   │   └──
│   ├── constants
│   │   └──
│   ├── containers
│   │   └──
│   ├── reducers
│   │   └──
│   ├── stylesheets
│   │   └──
│   └── index.js
├── .eslintignore
├── .eslintrc.json
├── package.json
└── README.md
```