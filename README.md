 React-Redux 7.1
//@ Quick Start
    React Redux is the official React binding for Redux. It lets your React components read data from a Redux store, and dispatch actions to the store to update data.

 //@Installation
 React Redux 7.1 requires React 16.8.3 or later.
 To use React Redux with your React app:   
 npm install react-redux

 @//Exmp

 Provider
React Redux provides <Provider />, which makes the Redux store available to the rest of your app:

import React from 'react'
import ReactDOM from 'react-dom'

import { Provider } from 'react-redux'
import store from './store'

import App from './App'

const rootElement = document.getElementById('root')
ReactDOM.render(
  <Provider store={store}>
    <App />
  </Provider>,
  rootElement
)

connect()
React Redux provides a connect function for you to connect your component to the store.

Normally, you’ll call connect in this way:

import { connect } from 'react-redux'
import { increment, decrement, reset } from './actionCreators'

// const Counter = ...

const mapStateToProps = (state /*, ownProps*/) => {
  return {
    counter: state.counter
  }
}

const mapDispatchToProps = { increment, decrement, reset }

export default connect(
  mapStateToProps,
  mapDispatchToProps
)(Counter)

//@ Basic Tutorial
To see how to use React Redux in practice, we’ll show a step-by-step example by creating a todo list app.
