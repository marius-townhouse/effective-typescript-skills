# Exhaustiveness Checking Example

This example shows how the `exhaustiveness-checking` skill catches missing cases.

## Without Skill

```typescript
type Shape = 
  | { kind: 'circle'; radius: number }
  | { kind: 'square'; side: number }
  | { kind: 'triangle'; base: number; height: number };

function getArea(shape: Shape): number {
  switch (shape.kind) {
    case 'circle':
      return Math.PI * shape.radius ** 2;
    case 'square':
      return shape.side ** 2;
    // Forgot triangle!
  }
}

// No error at compile time
// Runtime error if triangle is passed
```

## With Skill Applied

```typescript
type Shape = 
  | { kind: 'circle'; radius: number }
  | { kind: 'square'; side: number }
  | { kind: 'triangle'; base: number; height: number };

function assertUnreachable(x: never): never {
  throw new Error(`Didn't expect to get here: ${x}`);
}

function getArea(shape: Shape): number {
  switch (shape.kind) {
    case 'circle':
      return Math.PI * shape.radius ** 2;
    case 'square':
      return shape.side ** 2;
    // Error: 'triangle' is not handled!
    default:
      return assertUnreachable(shape);
      //     ^^^^^^^^ Error: Type 'triangle' is not assignable to 'never'
  }
}

// Fixed version
function getArea(shape: Shape): number {
  switch (shape.kind) {
    case 'circle':
      return Math.PI * shape.radius ** 2;
    case 'square':
      return shape.side ** 2;
    case 'triangle':
      return (shape.base * shape.height) / 2;
    default:
      return assertUnreachable(shape); // OK now
  }
}
```
