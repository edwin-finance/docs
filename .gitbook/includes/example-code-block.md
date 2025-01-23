---
title: Example code block
---

# Basic usage

1. Install the package:

```bash
pnpm install edwin-sdk
```

Use the package functionality:

```typescript
import { Edwin, EdwinConfig } from 'edwin-sdk';

// Configure Edwin wallets and providers
const edwinConfig: EdwinConfig = {
    evmPrivateKey: process.env.PRIVATE_KEY,
    solanaPrivateKey: process.env.SOLANA_PRIVATE_KEY,
    actions: ['supply', 'withdraw', 'stake']
};

// Initialize Edwin SDK
const edwin = new Edwin(edwinConfig);

// Supply tokens to a lending protocol
await edwin.actions.supply.execute({
    protocol: 'aave',
    chain: 'base',
    amount: '100',
    asset: 'usdc'
});
```
