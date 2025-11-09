---
title: Describing the UI
status: draft
last_reviewed: 09-11-2025
---

# Describing the UI

This section digs deeper into components, props, JSX patterns, and keeping components pure.

## Component Organization

- Keep components small and focused; break UIs into trees of reusable pieces.
- Use default exports for primary components; export helpers explicitly when needed.
- Co-locate component files near related assets for maintainability.

## Props & Data Flow

- Props are read-only inputs; destructure in the signature for clarity.

```jsx
function Avatar({ person, size }) {
  return (
    <img
      className="avatar"
      src={person.imageUrl}
      alt={person.name}
      width={size}
      height={size}
    />
  );
}
```

- Provide default values via destructuring (`function Avatar({ size = 100 }) { ... }`).
- Combine props when rendering lists (`{items.map(item => <Item {...item} />)}`).

## Conditional Rendering

- Prefer ternaries for inline decisions; lift logic out for readability when branching is complex.
- Return `null` to skip rendering without breaking component purity.

```jsx
function Alert({ message }) {
  if (!message) return null;
  return <p className="alert">{message}</p>;
}
```

## Rendering Lists & Keys

- Keys must be stable across renders; prefer unique IDs from data.
- Avoid array indexes as keys when list reordering/removal occurs.
- Wrap list items in fragments if no additional DOM nodes are needed.

```jsx
return items.map((item) => (
  <Fragment key={item.id}>
    <dt>{item.term}</dt>
    <dd>{item.definition}</dd>
  </Fragment>
));
```

## Keeping Components Pure

- Pure components: same inputs ⇒ same output, with no side effects during render.
- Do not mutate props or global state inside render; use events/effects for side effects.
- Avoid sharing mutable values between renders; rely on props and state instead.

## UI as a Tree

- Visualize component nesting to reason about data flow and state placement.
- Tools like React DevTools component tree viewer help identify re-render patterns.

## Practice Prompts

- Refactor a UI snippet into a component tree diagram, then implement components with props.
- Identify impure patterns (mutating props, conditional hook calls) and rewrite them as pure components.
- Build a glossary list that groups entries by category, ensuring keys remain stable.
