Handling function have to initial before `useOutsideClick` hook.

🌈 **Installation**:

-   **NPM**: `npm i reactjs-outside-click --save`
-   **YARN**: `yarn add reactjs-outside-click`

## Example

```
import React from 'react';
import useOutsideClick from 'reactjs-outside-click';

const HelloWorld = () => {
    const elementRef = useRef(null);
    const onOpenDiv = () => {
        setstate(prev => !prev);
    };
    useOutsideClick(testRef, onOpenDiv);
    return (
            <div ref={elementRef}>
                <button onClick={onOpenDiv}>Click</button>
                {state && <span>demo</span>}
            </div>
    );
};

export default HelloWorld;
```
