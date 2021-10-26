# hashids-test

A place to test the import/export for hashids

## Environment

Node 12, Typescript 3

## Import Syntax

An example of this lives under the `import` branch.

```typescript
import Hashids from 'hashids/cjs';

const hashids = new Hashids();
console.log(hashids.encode(42));
```

For this to work, we need to add the following settings to `tsconfig.json`,

```json
{
  "allowSyntheticDefaultImports": true,
  "esModuleInterop": true
}
```

You can also write this as

```typescript
import Hashids = require('hashids/cjs');
```

## Require syntax

An example of this lives under the `require` branch.

```typescript
const Hashids = require('hashids');

const hashids = new Hashids();
console.log(hashids.encode(42));
```

For this, we need to install the Node.js types from the `DefinitelyTyped` repository.

```bash
npm install --save-dev @types/node
```
