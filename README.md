# Effective TypeScript Skills

AI skills derived from **"Effective TypeScript" by Dan Vanderkam** (2nd Edition).

These skills follow the [code-craft](https://github.com/yanko-belov/code-craft) format and can be used with AI coding assistants to enforce TypeScript best practices.

## What Are AI Skills?

AI skills are structured instructions that guide AI assistants (like Claude Code, Cursor, etc.) to apply specific coding principles consistently. Each skill contains:

- **Triggers**: When to apply the skill
- **Iron Rule**: The core principle that must not be violated
- **Detection**: How to recognize when the skill applies
- **Pressure Resistance Protocol**: How to respond when pressured to violate the principle
- **Red Flags**: Warning signs that something is wrong
- **Quick Reference**: At-a-glance summary

## All 83 Skills

### Chapter 1: Getting to Know TypeScript (5 skills)

| Skill | Item | Description |
|-------|------|-------------|
| [ts-js-relationship](skills/ts-js-relationship/SKILL.md) | Item 1 | Understand the relationship between TypeScript and JavaScript |
| [tsconfig-options](skills/tsconfig-options/SKILL.md) | Item 2 | Know which TypeScript options you are using |
| [code-gen-independent](skills/code-gen-independent/SKILL.md) | Item 3 | Understand that code generation is independent of types |
| [structural-typing](skills/structural-typing/SKILL.md) | Item 4 | Understand duck typing and how TypeScript checks shape |
| [limit-any-type](skills/limit-any-type/SKILL.md) | Item 5 | Limit the use of `any` to preserve type safety |

### Chapter 2: TypeScript's Type System (12 skills)

| Skill | Item | Description |
|-------|------|-------------|
| [editor-interrogation](skills/editor-interrogation/SKILL.md) | Item 6 | Use your editor to interrogate the type system |
| [types-as-sets](skills/types-as-sets/SKILL.md) | Item 7 | Think of types as sets of values |
| [type-value-space](skills/type-value-space/SKILL.md) | Item 8 | Know how to tell whether a symbol is in type or value space |
| [prefer-type-annotations](skills/prefer-type-annotations/SKILL.md) | Item 9 | Prefer type annotations to type assertions |
| [avoid-wrapper-types](skills/avoid-wrapper-types/SKILL.md) | Item 10 | Avoid wrapper types (String, Number, Boolean) |
| [excess-property-checking](skills/excess-property-checking/SKILL.md) | Item 11 | Understand excess property checking |
| [function-type-expressions](skills/function-type-expressions/SKILL.md) | Item 12 | Apply types to functions with type expressions |
| [type-vs-interface](skills/type-vs-interface/SKILL.md) | Item 13 | Know the differences between type and interface |
| [use-readonly](skills/use-readonly/SKILL.md) | Item 14 | Use readonly to prevent accidental mutation |
| [dry-types](skills/dry-types/SKILL.md) | Item 15 | Use type operations to keep types DRY |
| [index-signature-alternatives](skills/index-signature-alternatives/SKILL.md) | Item 16 | Prefer arrays, tuples, or maps over index signatures |
| [avoid-numeric-index](skills/avoid-numeric-index/SKILL.md) | Item 17 | Avoid numeric index signatures when possible |

### Chapter 3: Type Inference and Control Flow (11 skills)

| Skill | Item | Description |
|-------|------|-------------|
| [avoid-inferable-annotations](skills/avoid-inferable-annotations/SKILL.md) | Item 18 | Avoid annotating types that TypeScript can infer |
| [different-variables-types](skills/different-variables-types/SKILL.md) | Item 19 | Understand that the same variable can have different types |
| [understand-type-widening](skills/understand-type-widening/SKILL.md) | Item 20 | Understand how type widening works |
| [create-objects-all-at-once](skills/create-objects-all-at-once/SKILL.md) | Item 21 | Create objects all at once to help type inference |
| [type-narrowing](skills/type-narrowing/SKILL.md) | Item 22 | Understand type narrowing with control flow |
| [consistent-aliases](skills/consistent-aliases/SKILL.md) | Item 23 | Be consistent in your use of type aliases |
| [context-type-inference](skills/context-type-inference/SKILL.md) | Item 24 | Understand context in type inference |
| [evolving-types](skills/evolving-types/SKILL.md) | Item 25 | Understand evolving types in arrays and objects |
| [functional-constructs-types](skills/functional-constructs-types/SKILL.md) | Item 26 | Use functional constructs and libraries to help with typing |
| [async-over-callbacks](skills/async-over-callbacks/SKILL.md) | Item 27 | Use async/await instead of raw promises |
| [currying-inference](skills/currying-inference/SKILL.md) | Item 28 | Understand how currying affects type inference |

### Chapter 4: Type Design (14 skills)

| Skill | Item | Description |
|-------|------|-------------|
| [valid-state-types](skills/valid-state-types/SKILL.md) | Item 29 | Design types that represent valid states only |
| [liberal-accept-strict-return](skills/liberal-accept-strict-return/SKILL.md) | Item 30 | Be liberal in what you accept and strict in what you produce |
| [no-type-in-docs](skills/no-type-in-docs/SKILL.md) | Item 31 | Don't put types in JSDoc - use TypeScript |
| [no-null-in-aliases](skills/no-null-in-aliases/SKILL.md) | Item 32 | Avoid null values in type aliases |
| [push-null-to-perimeter](skills/push-null-to-perimeter/SKILL.md) | Item 33 | Push null values to the perimeter of your API |
| [tagged-unions](skills/tagged-unions/SKILL.md) | Item 34 | Prefer tagged unions to hierarchical unions |
| [precise-string-types](skills/precise-string-types/SKILL.md) | Item 35 | Prefer more precise alternatives to string types |
| [distinct-special-values](skills/distinct-special-values/SKILL.md) | Item 36 | Use distinct types for special values |
| [limit-optional-properties](skills/limit-optional-properties/SKILL.md) | Item 37 | Limit the use of optional properties |
| [avoid-repeated-params](skills/avoid-repeated-params/SKILL.md) | Item 38 | Avoid repeated parameters of the same type |
| [unify-types](skills/unify-types/SKILL.md) | Item 39 | Prefer unifying types to modeling differences |
| [imprecise-over-inaccurate](skills/imprecise-over-inaccurate/SKILL.md) | Item 40 | Prefer imprecise types to inaccurate types |
| [domain-language-types](skills/domain-language-types/SKILL.md) | Item 41 | Name types using the language of your problem domain |
| [avoid-anecdotal-types](skills/avoid-anecdotal-types/SKILL.md) | Item 42 | Avoid types based on anecdotal data |

### Chapter 5: Unsoundness and the any Type (7 skills)

| Skill | Item | Description |
|-------|------|-------------|
| [narrow-any-scope](skills/narrow-any-scope/SKILL.md) | Item 43 | Use the narrowest possible scope for any types |
| [precise-any-variants](skills/precise-any-variants/SKILL.md) | Item 44 | Prefer more precise variants of any to plain any |
| [hide-unsafe-assertions](skills/hide-unsafe-assertions/SKILL.md) | Item 45 | Hide unsafe type assertions in well-typed functions |
| [prefer-unknown-over-any](skills/prefer-unknown-over-any/SKILL.md) | Item 46 | Use unknown instead of any for values with an unknown type |
| [type-safe-monkey-patching](skills/type-safe-monkey-patching/SKILL.md) | Item 47 | Prefer type-safe approaches to monkey patching |
| [soundness-traps](skills/soundness-traps/SKILL.md) | Item 48 | Avoid soundness traps |
| [type-coverage](skills/type-coverage/SKILL.md) | Item 49 | Track your type coverage to prevent regression |

### Chapter 6: Generics and Type-Level Programming (9 skills)

| Skill | Item | Description |
|-------|------|-------------|
| [generics-as-functions](skills/generics-as-functions/SKILL.md) | Item 50 | Think of generics as functions between types |
| [avoid-unnecessary-type-params](skills/avoid-unnecessary-type-params/SKILL.md) | Item 51 | Avoid unnecessary type parameters |
| [conditional-types-over-overloads](skills/conditional-types-over-overloads/SKILL.md) | Item 52 | Prefer conditional types to overload signatures |
| [control-union-distribution](skills/control-union-distribution/SKILL.md) | Item 53 | Control the distribution of unions over conditional types |
| [template-literal-types](skills/template-literal-types/SKILL.md) | Item 54 | Use template literal types to model DSLs |
| [test-your-types](skills/test-your-types/SKILL.md) | Item 55 | Write tests for your types |
| [type-display-attention](skills/type-display-attention/SKILL.md) | Item 56 | Pay attention to how types display |
| [tail-recursive-generics](skills/tail-recursive-generics/SKILL.md) | Item 57 | Prefer tail-recursive generic types |
| [codegen-over-complex-types](skills/codegen-over-complex-types/SKILL.md) | Item 58 | Consider codegen as an alternative to complex types |

### Chapter 7: TypeScript Recipes (6 skills)

| Skill | Item | Description |
|-------|------|-------------|
| [exhaustiveness-checking](skills/exhaustiveness-checking/SKILL.md) | Item 59 | Use never types to perform exhaustiveness checking |
| [iterate-objects-safely](skills/iterate-objects-safely/SKILL.md) | Item 60 | Know how to iterate over objects |
| [record-types-sync](skills/record-types-sync/SKILL.md) | Item 61 | Use Record types to keep values in sync |
| [variadic-tuple-types](skills/variadic-tuple-types/SKILL.md) | Item 62 | Use rest parameters and tuple types for variadic functions |
| [exclusive-or-properties](skills/exclusive-or-properties/SKILL.md) | Item 63 | Use optional never properties to model exclusive or |
| [branded-types](skills/branded-types/SKILL.md) | Item 64 | Use branded types for nominal typing |

### Chapter 8: Type Declarations and @types (7 skills)

| Skill | Item | Description |
|-------|------|-------------|
| [typescript-devdependencies](skills/typescript-devdependencies/SKILL.md) | Item 65 | Put TypeScript and @types in devDependencies |
| [three-versions-types](skills/three-versions-types/SKILL.md) | Item 66 | Understand the three versions involved in type declarations |
| [export-public-types](skills/export-public-types/SKILL.md) | Item 67 | Export all types that appear in public APIs |
| [tsdoc-comments](skills/tsdoc-comments/SKILL.md) | Item 68 | Use TSDoc for API comments |
| [callback-this-type](skills/callback-this-type/SKILL.md) | Item 69 | Provide a type for this in callbacks |
| [mirror-types](skills/mirror-types/SKILL.md) | Item 70 | Mirror types to sever dependencies |
| [module-augmentation](skills/module-augmentation/SKILL.md) | Item 71 | Use module augmentation to improve types |

### Chapter 9: Writing and Running Your Code (7 skills)

| Skill | Item | Description |
|-------|------|-------------|
| [ecmascript-over-typescript-features](skills/ecmascript-over-typescript-features/SKILL.md) | Item 72 | Prefer ECMAScript features to TypeScript features |
| [source-maps-debugging](skills/source-maps-debugging/SKILL.md) | Item 73 | Use source maps to debug TypeScript |
| [runtime-type-reconstruction](skills/runtime-type-reconstruction/SKILL.md) | Item 74 | Know how to reconstruct types at runtime |
| [dom-hierarchy](skills/dom-hierarchy/SKILL.md) | Item 75 | Understand the DOM hierarchy |
| [accurate-environment-model](skills/accurate-environment-model/SKILL.md) | Item 76 | Create an accurate model of your environment |
| [type-checking-vs-testing](skills/type-checking-vs-testing/SKILL.md) | Item 77 | Understand the relationship between type checking and unit testing |
| [compiler-performance](skills/compiler-performance/SKILL.md) | Item 78 | Pay attention to compiler performance |

### Chapter 10: Modernization and Migration (5 skills)

| Skill | Item | Description |
|-------|------|-------------|
| [write-modern-javascript](skills/write-modern-javascript/SKILL.md) | Item 79 | Write modern JavaScript |
| [ts-check-jsdoc-experiment](skills/ts-check-jsdoc-experiment/SKILL.md) | Item 80 | Use @ts-check and JSDoc to experiment with TypeScript |
| [allowjs-mixing](skills/allowjs-mixing/SKILL.md) | Item 81 | Use allowJs to mix TypeScript and JavaScript |
| [module-by-module-migration](skills/module-by-module-migration/SKILL.md) | Item 82 | Convert module by module up your dependency graph |
| [noimplicitany-completion](skills/noimplicitany-completion/SKILL.md) | Item 83 | Don't consider migration complete until you enable noImplicitAny |

## Quick Start

### For Claude Code Users

```bash
# Clone to your Claude skills directory
git clone https://github.com/YOUR_USERNAME/effective-typescript-skills.git ~/.claude/skills/effective-typescript

# Or copy just the skills
cp -r effective-typescript-skills/skills/* ~/.claude/skills/
```

### For OpenCode Users

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/effective-typescript-skills.git

# The skills are automatically available in the skills/ directory
```

### For Other AI Assistants

Copy the `skills/` directory contents to your AI assistant's skills folder.

## Usage

### With Claude Code

**Option 1: Global Installation (Recommended)**

```bash
# Clone to Claude's global skills directory
git clone https://github.com/YOUR_USERNAME/effective-typescript-skills.git ~/.claude/skills/effective-typescript

# Or create a symlink
ln -s /path/to/effective-typescript-skills ~/.claude/skills/effective-typescript
```

**Option 2: Per-Project Installation**

```bash
# In your project root
mkdir -p .claude/skills
cp -r /path/to/effective-typescript-skills/skills/* .claude/skills/
```

**Option 3: Using Claude Code Commands**

```bash
# In Claude Code, use the /skills command to load skills
# Or add to your .claude/AGENTS.md:
"""
You have access to the following skills from effective-typescript-skills:
- ts-js-relationship
- prefer-type-annotations
- avoid-unnecessary-type-params
- ... (all 83 skills)
"""
```

### With OpenCode

OpenCode automatically discovers skills in the `skills/` directory. Simply:

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/effective-typescript-skills.git

# The skills are immediately available in the skills/ directory
# OpenCode will load them automatically
```

### With Cursor

**Option 1: Cursor Rules**

Create a `.cursorrules` file in your project:

```markdown
# Effective TypeScript Skills

You are an expert TypeScript developer following the principles from "Effective TypeScript" by Dan Vanderkam.

Key principles:
- Prefer type annotations over type assertions
- Avoid unnecessary type parameters
- Use strictNullChecks and noImplicitAny
- Design types that make invalid states unrepresentable
- Export all types that appear in public APIs

Refer to the skills in: /path/to/effective-typescript-skills/skills/
```

**Option 2: Custom Instructions**

Go to Cursor Settings > General > Custom Instructions and paste the key principles from the skills.

### With Other AI Assistants

Copy the `skills/` directory to your AI assistant's configuration:

```bash
# Generic approach
cp -r effective-typescript-skills/skills/* ~/.config/YOUR_AI_ASSISTANT/skills/
```

## Book Reference

These skills are based on:

> **Effective TypeScript: 83 Specific Ways to Improve Your TypeScript**  
> by Dan Vanderkam  
> O'Reilly Media, 2nd Edition (2024)

The book covers TypeScript comprehensively across 10 chapters:
1. Getting to Know TypeScript
2. TypeScript's Type System
3. Type Inference and Control Flow Analysis
4. Type Design
5. `any` and Type Assertions
6. Generics and Type-Level Programming
7. TypeScript Recipes
8. Type Declarations and `@types`
9. Writing and Running Your Code
10. Modernization and Migration

## Skill Format

Each skill follows this structure:

```markdown
---
name: skill-name
description: Use when [trigger]. Use when [trigger].
---

# Skill Title

## Overview
Brief explanation of the principle.

## When to Use This Skill
- Situation 1
- Situation 2

## The Iron Rule
The core principle that must not be violated.

## Detection
How to recognize when this skill applies.

## Pressure Resistance Protocol
How to respond when pressured to violate the principle.

## Red Flags - STOP and Reconsider
Warning signs.

## Common Rationalizations (All Invalid)
Excuses people use to violate the principle.

## Quick Reference
At-a-glance summary table.

## The Bottom Line
One-sentence summary.

## Reference
Book citation.
```

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

To add a new skill:

1. Create a directory under `skills/` with the skill name
2. Add a `SKILL.md` file following the format above
3. Update this README with the new skill
4. Submit a pull request

## Book Reference

These skills are based on:

> **Effective TypeScript: 83 Specific Ways to Improve Your TypeScript**  
> by Dan Vanderkam  
> O'Reilly Media, 2nd Edition (2024)

Please purchase the book to support the author and get the full context behind these principles.

## License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file for details.

The skills are educational summaries and should be used alongside the original book.

## Acknowledgments

- Dan Vanderkam for writing "Effective TypeScript"
- The TypeScript team for creating an amazing language
- The code-craft project for the skill format inspiration
