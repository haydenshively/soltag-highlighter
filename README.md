# soltag-highlighter

Syntax highlighting for inline Solidity inside `` sol`...` `` tagged template literals in JavaScript and TypeScript.

## Features

- Solidity syntax highlighting inside `sol` tagged templates
- Supports `${...}` interpolations with JS/TS highlighting
- Supports `sol(...)` call syntax, e.g. `` sol(/* imports */)`...` ``
- Works in `.js`, `.ts`, `.jsx`, and `.tsx` files

## Usage

Write a tagged template with the `sol` tag and it will be highlighted as Solidity:

```ts
const contract = sol`
  pragma solidity ^0.8.0;

  contract Foo {
    uint256 public x;
  }
`;
```

Interpolations are highlighted as JS/TS:

```ts
const contract = sol`
  ${importSomeLibrary}

  contract Bar {
    uint256 public y;
  }
`;
```
