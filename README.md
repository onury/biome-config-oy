# biome-config-oy

Shared [Biome](https://biomejs.dev) (lint + format) base config. Replaces the
retired `eslint-config-oy` (the projects moved from ESLint to Biome).

## Usage

```jsonc
// biome.json
{
  "$schema": "https://biomejs.dev/schemas/2.5.0/schema.json",
  "extends": ["biome-config-oy"],
  "vcs": { "enabled": true, "clientKind": "git", "useIgnoreFile": true },
  "files": { "includes": ["src/**/*.ts", "test/**/*.ts", "*.ts"] }
}
```

Install alongside Biome:

```sh
npm i -D @biomejs/biome biome-config-oy
```

## Conventions

- 2-space indent, single quotes, semicolons, no trailing commas, width 100.
- `recommended` rules on, with project-style exceptions disabled
  (`noExplicitAny`, `noImplicitAnyLet`, `noConfusingVoidType`, `noSparseArray`,
  `useTemplate`, `noNonNullAssertion`, `noParameterAssign`, `noArguments`,
  `noUnusedFunctionParameters`, `noVoidTypeReturn`).
- Import organization enabled.

Each project sets its own `files.includes` and `vcs`.

### Related projects
- [`tsconfig-oy`](https://github.com/onury/tsconfig-oy)
- [`eslint-config-oy`](https://github.com/onury/eslint-config-oy)