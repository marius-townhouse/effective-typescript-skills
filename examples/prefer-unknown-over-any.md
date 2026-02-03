# TypeScript Type Safety Example

This example demonstrates how the `prefer-unknown-over-any` skill prevents unsafe code.

## Without Skill

```typescript
// User uses any for flexibility
function parseJSON(input: string): any {
  return JSON.parse(input);
}

// Later, this compiles but fails at runtime
const data = parseJSON('{"name": "John"}');
console.log(data.nane); // No error, but wrong property name!
```

## With Skill Applied

```typescript
// Skill enforces unknown instead
function parseJSON(input: string): unknown {
  return JSON.parse(input);
}

// Now TypeScript forces type checking
const data = parseJSON('{"name": "John"}');

// Error: Object is of type 'unknown'
console.log(data.name);

// Correct approach with type guard
interface User {
  name: string;
}

function isUser(value: unknown): value is User {
  return (
    typeof value === 'object' &&
    value !== null &&
    'name' in value &&
    typeof (value as Record<string, unknown>).name === 'string'
  );
}

if (isUser(data)) {
  console.log(data.name); // Safe!
}
```
