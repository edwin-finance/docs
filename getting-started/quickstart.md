---
icon: bullseye-arrow
---

# Quickstart

## Using Edwin Capabilities&#x20;

Edwin comes with a modular DeFAI system that can be used either stand alone or as part of an integration into an agent framework.

To use Edwin as a standalone package, follow these steps:

1. Install the Edwin package:

```bash
pnpm install edwin-sdk
```

2. Use the package functionality:

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

## Usage within an Agent

Choose an AI Agent framework - we will use elizaOS in this example.

1. Clone the Eliza repo from [https://github.com/elizaOS/eliza](https://github.com/elizaOS/eliza).
2. Inside the `packages` directory, clone the Edwin plugin for Eliza: [https://github.com/edwin-finance/eliza-plugin-edwin](https://github.com/edwin-finance/eliza-plugin-edwin)
3. Configure your `.env`with required secrets, and configure your agent character settings under `characters`.&#x20;
4. Run the agent and use DeFAI capabilities!
