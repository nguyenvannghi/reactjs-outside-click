Handling function have to initial before `useOutsideClick` hook.

🌈 **Installation**:

-   **NPM**: `npm i reactjs-outside-click --save`
-   **YARN**: `yarn add reactjs-outside-click`

## Example

```
import React, { useRef, useState } from "react";
import useOutsideClick from 'reactjs-outside-click';

const HelloWorld = () => {
  const [ state, setstate ] = useState(false);
  const elementRef = useRef(null);

  const onOpenDiv = () => {
    setstate(prev => !prev);
  };

  useOutsideClick(elementRef, onOpenDiv);
  return (
    <div className="App">
      <h1>Click outside to hide the element</h1>
      <div ref={elementRef}>
        <button onClick={onOpenDiv}>Click</button>
        {state && <span>demo</span>}
      </div>
    </div>
  );
};

export default HelloWorld;
```
