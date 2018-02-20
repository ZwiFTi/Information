# What makes react great

1. Its compositional model
2. Its declarative nature
3. The way data flows through a component
4. Its just JavaScript!


# compositional model

[Link 1](https://www.linkedin.com/pulse/compose-me-function-composition-javascript-kevin-greene/)
[Link 2](https://hackernoon.com/javascript-functional-composition-for-every-day-use-22421ef65a10)

# declarative

[Imperative vs declarative](https://tylermcginnis.com/imperative-vs-declarative-programming/)
[Imperative vs declarative 2](https://stackoverflow.com/questions/33655534/difference-between-declarative-and-imperative-in-react-js)


# Unidirectional data flow

Data flows one way, from parents down to children.


# Methods you need to know

`map()`
`filter()`


# SYNTAX

## Create element

What it does
React's .createElement() method takes in a description of an element and returns a plain JavaScript object.

The syntax
`React.createElement( /* type */, /* props */, /* content */ );`

`type` – either a string or a React Component
(This can be a string of any existing HTML element (e.g. 'p', 'span', or 'header') or you could pass a React component (we'll be creating components with JSX, in just a moment).)

`props` – either null or an object
(This is an object of HTML attributes and custom data about the element.)

`content` – `null`, a string, a React Element, or a React Component
Anything that you pass here will be the content of the rendered element. This can include plain text, JavaScript code, other React elements, etc.

DOM attributes supported by React:
https://reactjs.org/docs/dom-elements.html#all-supported-html-attributes

## Declaring Components in React

```
class ContactList extends React.Component {
// ...
}
```

[Rendering elements](https://reactjs.org/docs/rendering-elements.html)

# Install Facebooks create-react-app

`sudo npm install -g create-react-app`

# Creating a new app

`create-react-app <nameofapp>`

# Passing Data With props
Passing Data With Props Recap
A `prop` is any input that you pass to a React component. Just like an HTML attribute, a `prop` name and value are added to the Component.

```
// passing a prop to a component
<LogoutButton text='Wanna log out?' />
```
In the code above, `text` is the `prop` and the string `'Wanna log out?'` is the value.

All props are stored on the `this.props` object. So to access this `text` `prop` from inside the component, we'd use `this.props.text`:

```
// access the prop inside the component
...
render() {
    return <div>{this.props.text}</div>
}
...
```
[Props read](https://reactjs.org/docs/components-and-props.html)
