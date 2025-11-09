---
title: React Quick Start
status: draft
last_reviewed: 09-11-2025
---

# React Quick Start

This note captures the essentials from the official Quick Start, giving an overview of components, JSX, data display, events, and shared state.

## Components & Nesting

- Components are JavaScript functions returning JSX markup; names must be PascalCase (`MyButton`).
- Compose UI by nesting component tags (`<MyButton />`) inside parent components.
- Export a default component per file to make imports predictable.

```jsx
function MyButton() {
  return <button>I'm a button</button>;
}

export default function MyApp() {
  return (
    <div>
      <h1>Welcome to my app</h1>
      <MyButton />
    </div>
  );
}
```

## JSX Fundamentals

- JSX is stricter than HTML: close tags, wrap siblings in a single parent (`<>...</>`).
- Use `className` instead of `class`, `htmlFor` instead of `for`.
- Embed JavaScript expressions with `{}` for text, attributes, or inline styles.

```jsx
const user = {
  name: "Hedy Lamarr",
  imageUrl: "https://i.imgur.com/yXOvdOSs.jpg",
  imageSize: 90,
};

export default function Profile() {
  return (
    <>
      <h1>{user.name}</h1>
      <img
        className="avatar"
        src={user.imageUrl}
        alt={`Photo of ${user.name}`}
        style={{ width: user.imageSize, height: user.imageSize }}
      />
    </>
  );
}
```

## Rendering Lists & Conditions

- Render collections by mapping arrays to elements, providing a stable `key`.
- Use JavaScript control flow (`if`, ternary `? :`, logical `&&`) inside JSX.

```jsx
const products = [
  { title: "Cabbage", id: 1 },
  { title: "Garlic", id: 2 },
  { title: "Apple", id: 3 },
];

export default function ShoppingList() {
  return (
    <ul>
      {products.map((product) => (
        <li key={product.id}>{product.title}</li>
      ))}
    </ul>
  );
}
```

## Events & State

- Attach event handlers with camelCase props (`onClick={handleClick}`).
- `useState` returns `[state, setState]`; call setter to trigger re-render.
- Each instance of a component maintains its own state.

```jsx
import { useState } from "react";

function MyButton() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setCount(count + 1);
  }

  return <button onClick={handleClick}>Clicked {count} times</button>;
}
```

## Sharing Data Between Components

- Lift state to the nearest common ancestor.
- Pass state and setters down as props to synchronize child components.

```jsx
export default function App() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <MyButton count={count} onClick={() => setCount(count + 1)} />
      <MyButton count={count} onClick={() => setCount(count + 1)} />
    </div>
  );
}

function MyButton({ count, onClick }) {
  return <button onClick={onClick}>Clicked {count} times</button>;
}
```

## Practice Prompts

- Build a multi-button counter demo: one button updates its own state; another updates shared state.
- Convert an HTML snippet to JSX, paying attention to wrapper elements and attribute names.
- Render a list of objects with conditional formatting and ensure each item has a stable key.
