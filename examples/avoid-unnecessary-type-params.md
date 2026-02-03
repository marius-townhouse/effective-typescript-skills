# Generics Best Practices Example

This example demonstrates the `avoid-unnecessary-type-params` skill.

## Without Skill

```typescript
// Unnecessary generic - T only appears once
function parseYAML<T>(input: string): T {
  return JSON.parse(input) as T;
}

// Looks type-safe but isn't
const user: User = parseYAML('{}'); // No error, but empty object!
const bad: Banana = parseYAML('{}'); // Also "valid"
```

## With Skill Applied

```typescript
// Return unknown, force explicit handling
function parseYAML(input: string): unknown {
  return JSON.parse(input);
}

// User must explicitly assert or validate
const data = parseYAML('{"name": "John"}');

// Must use type assertion (acknowledging risk)
const user = parseYAML('{"name": "John"}') as User;

// Or better, validate at runtime
import { z } from 'zod';

const UserSchema = z.object({
  name: z.string(),
  email: z.string().email(),
});

const user = UserSchema.parse(parseYAML('...'));
// Type-safe and runtime-safe!
```
