# README

# Effective TypeScript Skills - Examples

This directory contains practical examples showing how each skill prevents common TypeScript mistakes.

## Examples by Chapter

### Chapter 3: Type Inference
- [avoid-unnecessary-type-params](avoid-unnecessary-type-params.md) - Why return-only generics are dangerous

### Chapter 5: Unsoundness and any
- [prefer-unknown-over-any](prefer-unknown-over-any.md) - Type-safe handling of unknown data

### Chapter 7: TypeScript Recipes
- [exhaustiveness-checking](exhaustiveness-checking.md) - Catching missing switch cases

## Running Examples

Each example shows:
1. **The Problem**: Code without the skill applied
2. **The Solution**: Code with the skill applied
3. **The Difference**: Why it matters

To try these yourself:
1. Copy the code into a TypeScript project
2. Enable `strict: true` in tsconfig.json
3. See the type errors appear (or not) based on the pattern used
