# ElementaryJS

ElementaryJS is JavaScript, but with sharp edges removed. We use it
in the Ocelot JavaScript IDE. For an overview of what ElementaryJS does,
[see this page](https://umass-compsci220.github.io/Ocelot/).

ElementaryJS is built on [Stopify](https://github.com/ocelot-ide/Stopify) to
facilitate interactive pedagogical use in browser-based applications (Ocelot);
among other things, it provides runtime safety checks (array bounds, function
arity, etc.) to protect users from common pitfalls encountered in "vanilla"
JavaScript (more details [here](https://www.ocelot-ide.org/rationale.html)) and
access to several useful helper functions that provide a gentle introduction to
APIs and design patterns.

## Building

On initialization (or when you update `package.json`):

    npm install

To build:

    npm run-script build

To lint:

    npm run-script lint

To test:

    npm run-script test

## Development

- `src/types.ts`: Types used throughout the codebase.

- `src/visitor.ts`: The heart of the ElementaryJS compiler. This code performs static checks and inserts dynamic checks that ElementaryJS enforces.

- `src/runtime.ts`: The ElementaryJS runtime system. This module has the implementations of the dynamic checks that the compiler inserts.

- `src/index.ts`: Entrypoint of the ElementaryJS package. This is the interface to ElementaryJS.

- `tests/`: Unit tests.

- `eval/`: Scripts and files used for evaluating ElementaryJS effectiveness.

## Unsupported Features

ElementaryJS does not support some JavaScript features, not because we intend to omit them, but because we haven't done the work to support them:

1. Array spread syntax
2. Destructuring assignment
