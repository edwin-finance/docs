---
icon: bullseye-arrow
---

# Quickstart

## Using edwin Capabilities

edwin comes with a modular DeFAI system that can be used either stand alone or as part of an integration into an agent framework.

To use edwin as a standalone package, follow these steps:

1. Install the edwin package:

```bash
pnpm install edwin-sdk
```

2. Use the package functionality:

```typescript
import { Edwin, EdwinConfig } from 'edwin-sdk';

// Configure Edwin wallets and providers
const edwinConfig: EdwinConfig = {
    evmPrivateKey: process.env.PRIVATE_KEY,
    solanaPrivateKey: process.env.SOLANA_PRIVATE_KEY
};

// Initialize Edwin SDK
const edwin = new Edwin(edwinConfig);

// Use a specific tool from a plugin
// Example: Using Aave supply tool
const result = await edwin.plugins.aave?.supply.execute({
    chain: 'base',
    asset: 'usdc',
    amount: 100
});
```

## Usage within an Agent

Choose an AI Agent framework - we will use elizaOS in this example.

1. Clone the Eliza repo from [https://github.com/elizaOS/eliza](https://github.com/elizaOS/eliza).
2. Inside the `packages` directory, clone the edwin plugin for Eliza: [https://github.com/edwin-finance/eliza-plugin-edwin](https://github.com/edwin-finance/eliza-plugin-edwin)
3. Configure your `.env` with required secrets:
   - `PRIVATE_KEY`: Your EVM private key
   - `SOLANA_PRIVATE_KEY`: Your Solana private key
   - `COOKIE_API_KEY`: (Optional) For Cookie plugin
   - `EORACLE_API_KEY`: (Optional) For EOracle plugin
   - `NFT_CONTRACT_ADDRESS`: (Optional) For Story Protocol plugin
   - `SPG_NFT_CONTRACT_ADDRESS`: (Optional) For Story Protocol plugin
4. Run the agent and use DeFAI capabilities!
