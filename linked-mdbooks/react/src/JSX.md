# JSX

- JSX = javascript extension format
- JSX syntax is not runnable in the webbrowser, since its not proper javascritp, it needs to be **_compiled_** (a JSX compiler will transform it into regular javascript!)

**JSX elements / expression**
```jsx
# regular
<h1>Hello World!</h1>   # looks like html but is found inside a js-file!

# with attributes**
<h1 class="mytitle">Hello World!</h1>   # added class-attribute 

# nested
<a href="https://www.example.com"><h1>Click me!</h1></a>

# nested multiline -> musst be wrapped in parenthesis
const theExample = (
  <a href="https://www.example.com">
    <h1>
      Click me!
    </h1>
  </a>
);
```
- a JSX expression must have exactly one outermost element. If this seems unreasonable just put a `<div></div>` tag around it!

**Rendering JSX expressions**
`ReactDOM` is a Javascript library which contains several React-specific methods, all of which deal with the DOM in some way or another.
- `ReactDOM.render(arg1, arg2)`: `arg1` is a JSX Expression. `arg2` is the place where the compiled JSX Expression should be rendered. Example:
```js
ReactDOM.render(<h1>Hello World</h1>, document.getElementById('some_id'));
```
`ReactDOM.render()` only updates DOM elements that have changed (very efficient)!




# class / className
- `class` in html -> `className` in JSX!!
- why? because JSX gets rendered to JS and in JS `class` is a reserved word!

# self-closing tags
- in JSX you have to add a slash to selfclosing tags!
```js
# ok in html
<br>
# in JSX:
<br/>
```

# Curly Braces in JSX
- curly braces say: "Even though I am located in between JSX tags, treat me like ordinary JavaScript and not like JSX."
- javascript injection to JSX!

# inject Variables in JSX
- When injecting JavaScript into JSX, that JavaScript is part of the same environment as the rest of the JS in the file.
- access variables while inside of a JSX expression, even if those variables were declared on the outside.

# event listeners
- You create an event listener by giving a JSX element a special attribute. Here's an example
```jsx
# JSX element with click functionality 
<img onClick={myFunc} />
```
Syntax is always `on` + `EventName`. Here are some of the attributes you can use as event ([documentation with all possible Events](https://reactjs.org/docs/events.html)). Note that in HTML, event listener names are written in all lowercase, such as `onclick` or `onmouseover`. In JSX, event listener names are written in camelCase, such as `onClick` or `onMouseOver`. 
```jsx
onClick
onDubleClick
onMouseOver
onMouseMove
```


# JSX Conditional Statements
- if statements break in JSX. Other options:
  - if works if the `if` and `else` are not injected in JSX (when JSX code is written outside of it-else)
  - ternary operator
  - &&
  - 

