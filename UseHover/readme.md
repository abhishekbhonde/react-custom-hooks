# Hover Hook
================

## Overview
The `useHover` hook is a reusable React hook that provides a way to detect when an element is hovered over. It uses the `useState` and `useEffect` hooks to track the hover state and attach event listeners to the element.

## Usage
Here are two use cases for the `useHover` hook:

### Use Case 1: Hover Effects
The `useHover` hook can be used to create hover effects in an application. For example, you can change the color or style of an element when it is hovered over.

### Use Case 2: Interactive Elements
The `useHover` hook can be used to create interactive elements that respond to hover events. For example, you can display a tooltip or a popup when an element is hovered over.

### Example
```jsx
import React from 'react';
import useHover from './useHover';

const App = () => {
    const [hoverRef, isHovered] = useHover();

    return (
        <div>
            <h1 ref={hoverRef} style={{ color: isHovered ? 'blue' : 'black' }}>
                Hover over me!
            </h1>
        </div>
    );
};

export default App;
```

## Functionality
- The `useHover` hook initializes the hover state with `false`.
- The hook uses the `useState` hook to track the hover state.
- The hook uses the `useEffect` hook to attach event listeners to the element.
- The event listeners are removed when the component is unmounted.
- The hook returns a reference to the element and the hover state.

## Props
- `ref`: A reference to the element to which the hook should be applied.
- `isHovered`: The current hover state of the element.

## Usage Tips
- Use the `useHover` hook in conjunction with the `useState` hook to track the hover state.
- Use the `useEffect` hook to attach event listeners to the element.
- Use the `ref` returned by the hook to access the element.
- Use the `isHovered` returned by the hook to conditionally apply styles or effects.