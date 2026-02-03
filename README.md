# Effective TypeScript Skills

AI skills derived from **"Effective TypeScript" by Dan Vanderkam** (2nd Edition) - 83 specific ways to improve your TypeScript.

These skills help AI coding assistants (Claude Code, OpenCode, Cursor, etc.) write better TypeScript by following the best practices from the book.

## What Are These?

**Skills** are documents that teach AI assistants to resist common TypeScript anti-patterns and produce higher quality code. Unlike documentation, these skills:

- **Resist pressure** - Handle "just use `any`" or "don't overcomplicate" requests
- **Close loopholes** - Address specific rationalizations AI uses to violate principles  
- **Provide correct patterns** - Show the right way, not just explain what's wrong

Each skill follows the proven format from [code-craft](https://github.com/yanko-belov/code-craft) with Iron Rules, Pressure Resistance Protocols, and Red Flags.

## Installation

### Using npx (Recommended)

```bash
# Install all skills to all supported agents
npx skills add marius-townhouse/effective-typescript-skills --all

# Install specific skills only
npx skills add marius-townhouse/effective-typescript-skills -s prefer-unknown-over-any exhaustiveness-checking

# Install to specific agents
npx skills add marius-townhouse/effective-typescript-skills -a opencode claude-code

# List available skills
npx skills add marius-townhouse/effective-typescript-skills -l
```

### Manual Installation

```bash
# Clone the repository
git clone https://github.com/marius-townhouse/effective-typescript-skills.git

# Symlink to your agent's skills directory
# For Claude Code:
ln -sf "$(pwd)/effective-typescript-skills/skills"/* ~/.claude/skills/

# For OpenCode:
ln -sf "$(pwd)/effective-typescript-skills" ~/.opencode/skills/effective-typescript
```

### Supported Agents

- OpenCode
- Claude Code
- Cursor
- GitHub Copilot (via .cursorrules)
- Any agent that reads markdown skill files

## Skills

### Chapter 1: Getting to Know TypeScript

| Skill | Item | Prevents |
|-------|------|----------|
| [ts-js-relationship](skills/ts-js-relationship/SKILL.md) | Item 1 | Misunderstanding TS/JS relationship |
| [tsconfig-options](skills/tsconfig-options/SKILL.md) | Item 2 | Using wrong compiler options |
| [code-gen-independent](skills/code-gen-independent/SKILL.md) | Item 3 | Confusing types with runtime |
| [structural-typing](skills/structural-typing/SKILL.md) | Item 4 | Nominal typing assumptions |
| [limit-any-type](skills/limit-any-type/SKILL.md) | Item 5 | `any` type abuse |

### Chapter 2: TypeScript's Type System

| Skill | Item | Prevents |
|-------|------|----------|
| [editor-interrogation](skills/editor-interrogation/SKILL.md) | Item 6 | Not using IDE for type exploration |
| [types-as-sets](skills/types-as-sets/SKILL.md) | Item 7 | Misunderstanding type semantics |
| [type-value-space](skills/type-value-space/SKILL.md) | Item 8 | Confusing type/value contexts |
| [prefer-type-annotations](skills/prefer-type-annotations/SKILL.md) | Item 9 | Unsafe type assertions |
| [avoid-wrapper-types](skills/avoid-wrapper-types/SKILL.md) | Item 10 | Using String/Number/Boolean |
| [excess-property-checking](skills/excess-property-checking/SKILL.md) | Item 11 | Excess property confusion |
| [function-type-expressions](skills/function-type-expressions/SKILL.md) | Item 12 | Incorrect function typing |
| [type-vs-interface](skills/type-vs-interface/SKILL.md) | Item 13 | Wrong type vs interface choice |
| [use-readonly](skills/use-readonly/SKILL.md) | Item 14 | Accidental mutations |
| [dry-types](skills/dry-types/SKILL.md) | Item 15 | Duplicated type definitions |
| [index-signature-alternatives](skills/index-signature-alternatives/SKILL.md) | Item 16 | Unsafe index signatures |
| [avoid-numeric-index](skills/avoid-numeric-index/SKILL.md) | Item 17 | Numeric index abuse |

### Chapter 3: Type Inference and Control Flow

| Skill | Item | Prevents |
|-------|------|----------|
| [avoid-inferable-annotations](skills/avoid-inferable-annotations/SKILL.md) | Item 18 | Unnecessary type annotations |
| [different-variables-types](skills/different-variables-types/SKILL.md) | Item 19 | Variable type confusion |
| [understand-type-widening](skills/understand-type-widening/SKILL.md) | Item 20 | Type widening surprises |
| [create-objects-all-at-once](skills/create-objects-all-at-once/SKILL.md) | Item 21 | Poor type inference |
| [type-narrowing](skills/type-narrowing/SKILL.md) | Item 22 | Missing type guards |
| [consistent-aliases](skills/consistent-aliases/SKILL.md) | Item 23 | Inconsistent type aliases |
| [context-type-inference](skills/context-type-inference/SKILL.md) | Item 24 | Contextual typing issues |
| [evolving-types](skills/evolving-types/SKILL.md) | Item 25 | Evolving type confusion |
| [functional-constructs-types](skills/functional-constructs-types/SKILL.md) | Item 26 | Poor functional typing |
| [async-over-callbacks](skills/async-over-callbacks/SKILL.md) | Item 27 | Callback hell |
| [currying-inference](skills/currying-inference/SKILL.md) | Item 28 | Currying type issues |

### Chapter 4: Type Design

| Skill | Item | Prevents |
|-------|------|----------|
| [valid-state-types](skills/valid-state-types/SKILL.md) | Item 29 | Invalid state representation |
| [liberal-accept-strict-return](skills/liberal-accept-strict-return/SKILL.md) | Item 30 | Wrong input/output types |
| [no-type-in-docs](skills/no-type-in-docs/SKILL.md) | Item 31 | Types in JSDoc |
| [no-null-in-aliases](skills/no-null-in-aliases/SKILL.md) | Item 32 | Null in type aliases |
| [push-null-to-perimeter](skills/push-null-to-perimeter/SKILL.md) | Item 33 | Null everywhere |
| [tagged-unions](skills/tagged-unions/SKILL.md) | Item 34 | Poor union design |
| [precise-string-types](skills/precise-string-types/SKILL.md) | Item 35 | Vague string types |
| [distinct-special-values](skills/distinct-special-values/SKILL.md) | Item 36 | Ambiguous special values |
| [limit-optional-properties](skills/limit-optional-properties/SKILL.md) | Item 37 | Optional property abuse |
| [avoid-repeated-params](skills/avoid-repeated-params/SKILL.md) | Item 38 | Confusing parameter order |
| [unify-types](skills/unify-types/SKILL.md) | Item 39 | Unnecessary type variants |
| [imprecise-over-inaccurate](skills/imprecise-over-inaccurate/SKILL.md) | Item 40 | Overly precise types |
| [domain-language-types](skills/domain-language-types/SKILL.md) | Item 41 | Poor type naming |
| [avoid-anecdotal-types](skills/avoid-anecdotal-types/SKILL.md) | Item 42 | Types from limited data |

### Chapter 5: Unsoundness and the any Type

| Skill | Item | Prevents |
|-------|------|----------|
| [narrow-any-scope](skills/narrow-any-scope/SKILL.md) | Item 43 | Wide any types |
| [precise-any-variants](skills/precise-any-variants/SKILL.md) | Item 44 | Plain any abuse |
| [hide-unsafe-assertions](skills/hide-unsafe-assertions/SKILL.md) | Item 45 | Exposed unsafe assertions |
| [prefer-unknown-over-any](skills/prefer-unknown-over-any/SKILL.md) | Item 46 | any instead of unknown |
| [type-safe-monkey-patching](skills/type-safe-monkey-patching/SKILL.md) | Item 47 | Unsafe monkey patching |
| [soundness-traps](skills/soundness-traps/SKILL.md) | Item 48 | Soundness issues |
| [type-coverage](skills/type-coverage/SKILL.md) | Item 49 | Type coverage regression |

### Chapter 6: Generics and Type-Level Programming

| Skill | Item | Prevents |
|-------|------|----------|
| [generics-as-functions](skills/generics-as-functions/SKILL.md) | Item 50 | Misunderstanding generics |
| [avoid-unnecessary-type-params](skills/avoid-unnecessary-type-params/SKILL.md) | Item 51 | Unnecessary type parameters |
| [conditional-types-over-overloads](skills/conditional-types-over-overloads/SKILL.md) | Item 52 | Overload overuse |
| [control-union-distribution](skills/control-union-distribution/SKILL.md) | Item 53 | Union distribution issues |
| [template-literal-types](skills/template-literal-types/SKILL.md) | Item 54 | Poor string type modeling |
| [test-your-types](skills/test-your-types/SKILL.md) | Item 55 | Untested type logic |
| [type-display-attention](skills/type-display-attention/SKILL.md) | Item 56 | Poor type display |
| [tail-recursive-generics](skills/tail-recursive-generics/SKILL.md) | Item 57 | Deep type recursion |
| [codegen-over-complex-types](skills/codegen-over-complex-types/SKILL.md) | Item 58 | Overly complex types |

### Chapter 7: TypeScript Recipes

| Skill | Item | Prevents |
|-------|------|----------|
| [exhaustiveness-checking](skills/exhaustiveness-checking/SKILL.md) | Item 59 | Missing union cases |
| [iterate-objects-safely](skills/iterate-objects-safely/SKILL.md) | Item 60 | Unsafe object iteration |
| [record-types-sync](skills/record-types-sync/SKILL.md) | Item 61 | Out of sync types |
| [variadic-tuple-types](skills/variadic-tuple-types/SKILL.md) | Item 62 | Poor variadic typing |
| [exclusive-or-properties](skills/exclusive-or-properties/SKILL.md) | Item 63 | Invalid property combos |
| [branded-types](skills/branded-types/SKILL.md) | Item 64 | Nominal type issues |

### Chapter 8: Type Declarations and @types

| Skill | Item | Prevents |
|-------|------|----------|
| [typescript-devdependencies](skills/typescript-devdependencies/SKILL.md) | Item 65 | Wrong dependency types |
| [three-versions-types](skills/three-versions-types/SKILL.md) | Item 66 | Version mismatches |
| [export-public-types](skills/export-public-types/SKILL.md) | Item 67 | Missing type exports |
| [tsdoc-comments](skills/tsdoc-comments/SKILL.md) | Item 68 | Poor API docs |
| [callback-this-type](skills/callback-this-type/SKILL.md) | Item 69 | Untyped this context |
| [mirror-types](skills/mirror-types/SKILL.md) | Item 70 | Tight coupling |
| [module-augmentation](skills/module-augmentation/SKILL.md) | Item 71 | Poor type extension |

### Chapter 9: Writing and Running Your Code

| Skill | Item | Prevents |
|-------|------|----------|
| [ecmascript-over-typescript-features](skills/ecmascript-over-typescript-features/SKILL.md) | Item 72 | TS-specific features |
| [source-maps-debugging](skills/source-maps-debugging/SKILL.md) | Item 73 | Debugging compiled JS |
| [runtime-type-reconstruction](skills/runtime-type-reconstruction/SKILL.md) | Item 74 | Runtime type issues |
| [dom-hierarchy](skills/dom-hierarchy/SKILL.md) | Item 75 | Wrong DOM types |
| [accurate-environment-model](skills/accurate-environment-model/SKILL.md) | Item 76 | Missing environment types |
| [type-checking-vs-testing](skills/type-checking-vs-testing/SKILL.md) | Item 77 | Types vs tests confusion |
| [compiler-performance](skills/compiler-performance/SKILL.md) | Item 78 | Slow compilation |

### Chapter 10: Modernization and Migration

| Skill | Item | Prevents |
|-------|------|----------|
| [write-modern-javascript](skills/write-modern-javascript/SKILL.md) | Item 79 | Outdated JS patterns |
| [ts-check-jsdoc-experiment](skills/ts-check-jsdoc-experiment/SKILL.md) | Item 80 | No TS experimentation |
| [allowjs-mixing](skills/allowjs-mixing/SKILL.md) | Item 81 | All-or-nothing migration |
| [module-by-module-migration](skills/module-by-module-migration/SKILL.md) | Item 82 | Wrong migration order |
| [noimplicitany-completion](skills/noimplicitany-completion/SKILL.md) | Item 83 | Incomplete migration |

**Total: 83 skills**

## How Skills Work

Each skill follows a consistent structure:

| Section | Purpose |
|---------|---------|
| **Iron Rule** | The non-negotiable principle |
| **Detection** | How to recognize violations |
| **Correct Pattern** | Code examples of the right way |
| **Pressure Resistance** | Handling pushback scenarios |
| **Red Flags** | Warning signs to watch for |
| **Rationalizations** | Common excuses and rebuttals |

### Example: Prefer unknown over any

**Without skill:**
```
User: "Parse this JSON and return the result"

Claude: *Returns any type*
"Here's your parsed data: any"
// User gets no type safety, silent failures possible
```

**With skill:**
```
User: "Parse this JSON and return the result"

Claude: *Returns unknown with type guard example*
"I've returned unknown to ensure type safety. 
You'll need to validate the structure using a type guard 
or schema validation (like zod)."
```

## Skill Categories

| Category | Skills | Focus |
|----------|--------|-------|
| **Fundamentals** | 5 | TypeScript basics |
| **Type System** | 12 | Understanding types |
| **Inference** | 11 | Type inference patterns |
| **Design** | 14 | Type architecture |
| **Safety** | 7 | any and soundness |
| **Generics** | 9 | Type-level programming |
| **Recipes** | 6 | Practical patterns |
| **Declarations** | 7 | Type definitions |
| **Runtime** | 7 | Running TypeScript |
| **Migration** | 5 | Adoption strategies |

## Examples

See the [examples/](examples/) directory for practical demonstrations of skills in action.

## Book Reference

These skills are based on:

> **Effective TypeScript: 83 Specific Ways to Improve Your TypeScript**  
> by Dan Vanderkam  
> O'Reilly Media, 2nd Edition (2024)

Please purchase the book to support the author and get the full context behind these principles.

## Contributing

Contributions welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Adding a New Skill

1. Create directory under `skills/` with kebab-case name
2. Add `SKILL.md` following the format
3. Update this README
4. Submit a pull request

## License

MIT License - see [LICENSE](LICENSE) file.

The skills are educational summaries and should be used alongside the original book.

## Acknowledgments

- Dan Vanderkam for "Effective TypeScript"
- [code-craft](https://github.com/yanko-belov/code-craft) for the skill format
- The TypeScript team for an amazing language
