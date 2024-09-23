Frontend part (considers source code):
- Scanning / lexing / lexical analysis
  Finding tokens & lexemes
- Parsing 
  Forming Parse Tree / Abstract Syntax Tree / Syntax Tree / ASTs / Tree
  Finding Syntax errors
- Static analysis (different for different languages)
  Binding / resolution (scopes, identifiers)
  Type checking (Type Error)
  Symbol table

Intermediate language
Can be used for multiple languages (C, Pascal -> IR, IR -> x86, ARM)

Optimizations:
- Constant folding (`a = 2*(6/3)` -> `a = 4`)

Backend part (considers the final platform):
- Code generation
  Generate p-code / bytecode (code for VM)

Can write VM (that translates bytecode at runtime, slow, but easy)
Can write compiler to native code  (fast, but hard)

Runtime provides low-level services:
- GC
- instance of checks

Runtime may be embedded into executable, or be a part of VM.

Shortcuts:
- Single-pass compiler
  Produce final code in parse phase
- Tree-walk interpreter
- Transpiler / source-to-source compiler 
- JIT compilation


```
 
```

Regular language - language that can be defined by a regular expression.

Chomsky hierarchy

Context-free grammar (CFG)

Backus-Naur form (BNF)

Extended BNF (EBNF) notation

## Parsers

LL(k)
LR(1)
LALR
Recursive descent

Spatial locality, temporal locality