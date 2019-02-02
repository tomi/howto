# Importing JSON files with TypeScript

Starting with [version 2.9](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-2-9.html), TypeScript supports importing JSON files type safely [out-of-the-box](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-2-9.html#new---resolvejsonmodule).

Required config:

1. In tsconfig.json, add

```json
{
  "compilerOptions": {
    // Emit __importStar and __importDefault helpers for runtime babel
    // ecosystem compatibility and enable --allowSyntheticDefaultImports
    // for typesystem compatibility.
    "esModuleInterop": true,
    // Include modules imported with .json extension.
    "resolveJsonModule": true
  }
}
```

2. Make sure the json file is included and not excluded
