# Epic React

## React Fundamentals

### _Exercise 1 - Hello World using vanilla JavaScript_

It's essential to understand how to manipulate DOM nodes with pure JavaScript before jumping into React.

This exercise let us practice DOM manipulations such as element's creation, setting different kinds of attributes into elements, such as `id`, `textContent`, and `className`, and append elements to the DOM. This means that even with an "empty" HTML, with can still "tell" the browser what to render and make interactive web pages.

### _Exercise 2 - Hello World using React and `ReactDOM` APIs_

As it is crucial to understand how to manipulate the DOM through its JavaScript API, this also applies to understand React's APIs before jumping into JSX.

While we use React to create elements, `ReactDOM` is used to render those elements into the DOM. They are separate things on purpose, and there are libraries such as `ReactNative`, which renders things on native apps instead of web browsers.

The property children used when creating a React component can accept a simple string, which defines the content of that element, or an array of sub-elements.

When it's time to grab the parent element to render our components into the DOM, we still use pure JavaScript to query the 'root' element `(document.getElementById('root')`).

For exercise purposes, it's ok to add React into a `script` tag. When running software in production, other approaches are recommended.

Components are reusable pieces of code that can compose web applications.

### _Exercise 3 - JSX and Babel_
JSX is a JS syntax sugar that allows us to create React components in a cleaner and more imperative way. JSX is powered by Babel, which transpile the code that the browser cannot understand into JavaScript code (e.g., `<MyDiv />` into `React.createElement('div')`).

We also import Babel inside of a script tag only for exercise purposes.

Babel's transpilation allows us to spread `props` into React components. It enables using any modern JavaScript logic (ES6+), such as template literals, shorthand property names, object, or array destructuring, etc.

To use Babel imported from a `script` tag, we use `<script type="text/babel">` instead of `type="module"`, besides its own tag with the `src` attribute.

### _Exercise 4 - Components as functions and PropTypes_

React components are functions that return renderable elements or other components.

`PropTypes` can validate the types of properties passed to Components to expose their interface to developers consuming them and enforcing required `props`.

`PropTypes` can also be imported inside of a `script` tag for exercise purposes.

### _Exercise 5 - Styling React Components_

The two most common ways of styling React Components are either inline CSS or CSS files and `className`s.
For reusability purposes, React components should expose a straightforward API and defined default values when they're not provided.

The order of the `...rest` operator matters. If we want to allow our components to be "customized," it should go after the defaults. On the other hand, if we're going to enforce defaults, they should come first so that the defaults would override them.

When defining some default stylings but allowing for extension, the spread operator can be used instead of `Object.assign`, making the code more imperative.

CSS files can be imported inside JS code as we would import CSS into HTML with the `<style>` tag.

React components are exported as modules.

Interpolation allows us to navigate from JSX into JS or CSS in JS lands, and then back.

### _Exercise 6 - Forms_

In React, forms aren't that different from HTML and JavaScript, although, when building SPAs, we can prevent the default browser refresh on form submission (`event.preventDefault()`).

Form components in React should receive event handlers as `props`.

Internally, we can handle form submission, changes in input elements, etc.

There are different ways of grabbing the value of the input fields. Some of them are fragile (e.g., `event.target.elements[0].value`), while others are more reliable (e.g., `event.target.elements.[inputFieldIdOrName].value`).

As in pure HTML, React components should be built with accessibility in mind, and it's essential to associate labels with inputs via `htmlFor` and `id`.

An alternative to getting the value of input fields through `event.target.elements...value` is to use `useRef`'s React Hook, which creates a reference to the element with a default value on the element through `ref={inputElementRef}`.

`useState`'s React Hook can be used on forms to solve different problems, such as defining an `error` state with its `setError` mechanism for changing the state or for determining the value of an input element, to mention a few examples.

Better than showing errors to our users telling them what is not allowed (such as uppercase characters on an input field), better to let them do it the way they feel comfortable and normalizing the data on the client-side (e.g., `event.target.value.toLowerCase()`).

### _Exercise 7 - The `key` property on React lists_

In React, the `key` property is used in lists as a mechanism for keeping track of the right elements, especially in cases of event handlers such as `onClick` that add or remove elements to/from a list.

The value of every `key` property should be unique, ideally being identified by an `id`.

___

Written with 💙 by [Walmyr Filho](https://walmyr.dev).
