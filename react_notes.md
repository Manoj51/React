# React Notes

From the react tuorial on the home page.

**Building blocks of react apps** :
* Elements
* Components

## JSX
* JSX produces React “elements”.
* You can embed any JavaScript expression in JSX by wrapping it in curly braces.
* We split JSX over multiple lines for readability. While it isn’t required, when doing this, we also recommend wrapping it in parentheses to avoid the pitfalls of automatic semicolon insertion.
* After compilation, JSX expressions become regular JavaScript objects.
* You may use quotes to specify string literals as attributes:
* You may also use curly braces to embed a JavaScript expression in an attribute:
* Since JSX is closer to JavaScript than HTML, React DOM uses camelCase property naming convention instead of HTML attribute names.
* JSX tags may contain children:
* Babel compiles JSX down to React.createElement() calls.

## Rendering Elements
* Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.
* Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.
* React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.
* React Only Updates What’s Necessary. React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

## Components and Props
* Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.
* Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.
#### Functional and Class Components
* The simplest way to define a component is to write a JavaScript function
* You can also use an ES6 class to define a component
#### Rendering a Component
* Previously, we only encountered React elements that represent DOM tags, However, elements can also represent user-defined components.
#### Composing Components
* Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail.

 Props are Read-Only
* Whether you declare a component as a function or a class, it must never modify its own props.
* All React components must act like pure functions with respect to their props.

## State and Lifecycle
* components defined as classes have some additional features. Local state is exactly that: a feature available only to classes.
* We want to set up a timer whenever the Clock is rendered to the DOM for the first time. This is called “mounting” in React.
* We also want to clear that timer whenever the DOM produced by the Clock is removed. This is called “unmounting” in React.
* We can declare special methods on the component class to run some code when a component mounts and unmounts
* These methods are called “lifecycle hooks”.
#### Using State Correctly
* Do Not Modify State Directly
* State Updates May Be Asynchronous
* State Updates are Merged
* The Data Flows Down
## Handling Events
* Handling events with React elements is very similar to handling events on DOM elements. There are some syntactic differences
* Another difference is that you cannot return false to prevent default behavior in React. You must call preventDefault explicitly.
## Conditional rendering
* In React, you can create distinct components that encapsulate behavior you need. Then, you can render only some of them, depending on the state of your application.
#### Preventing Component from Rendering
* In rare cases you might want a component to hide itself even though it was rendered by another component. To do this return null instead of its render output.
* Returning null from a component’s render method does not affect the firing of the component’s lifecycle methods.
## Lists and Keys
* Usually you would render lists inside a component.
* A “key” is a special string attribute you need to include when creating lists of elements.
* Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity
* Keys Must Only Be Unique Among Siblings
## Forms
* HTML form elements work a little bit differently from other DOM elements in React, because form elements naturally keep some internal state.
#### Controlled Components
* An input form element whose value is controlled by React in this way is called a “controlled component”.
## Lifting State Up
* 