# basic seup
```jsx
import React from 'react'
import ReactDOM from 'react-dom'

ReactDOM.render(<h1>helloWorld</h1>, document.getElementById('root'));
```

# Functional Components
- packed inside a function
```jsx
import React from 'react'
import ReactDOM from 'react-dom'

const root = document.getElementById("root");

const App = () => {
  const name = 'Hello World';
  return (
    <h1>{name}</h1>
  );
};

ReactDOM.render(<App />, root);
```

