---
icon: hand-wave
cover: https://gitbookio.github.io/onboarding-template-images/header.png
coverY: 0
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Hello Edwin

<figure><img src=".gitbook/assets/office 2.jpg" alt=""><figcaption></figcaption></figure>

### The Missing Bridge in DeFAI

The world of finance is experiencing two parallel revolutions. AI frameworks like [LangChain](https://github.com/langchain-ai/langchain), [Eliza](https://github.com/elizaos/eliza), and [G.A.M.E](https://github.com/game-by-virtuals/game-python/tree/main) have transformed software development, creating autonomous agents that reason and execute complex tasks. Simultaneously, DeFi protocols like [Aave](https://aave.com/), [Uniswap](https://uniswap.org/), and [Morpho](https://morpho.xyz/) have built an open, programmable financial system managing billions in assets. Yet a critical gap exists - AI frameworks excel at decision-making but lack native DeFi capabilities, while DeFi protocols remain isolated from AI systems. Each protocol speaks its own language, uses unique interfaces, and requires specialized knowledge to integrate, creating a barrier between these two revolutionary technologies.

### What is Edwin?

Edwin enables AI agents built on top of AI frameworks to seamlessly interact with DeFi protocols. By providing a universal interface and handling blockchain operations securely, Edwin serves as the infrastructure layer that bridges the gap between AI and DeFi, unlocking the potential of autonomous financial operations - DeFAI.

<figure><img src=".gitbook/assets/lecture 1.jpg" alt=""><figcaption></figcaption></figure>

### Architecture

Edwin consists of several core components that work together to enable DeFAI operations:

#### Core Components

* **Protocol Abstraction Layer**: Unified interface for DeFi operations
* **Framework Adapters**: Integration with AI frameworks
* **Security Layer**: Transaction verification and execution

<figure><img src=".gitbook/assets/Edwin Diagram (6).png" alt=""><figcaption></figcaption></figure>

#### Current Integrations

AI Frameworks:

* Eliza

Blockchains:

* Solana
* EVM

DeFi Protocols:

* Lending: Aave
* DEX: Uniswap

### Getting Started

```bash
pnpm install edwin-sdk
```

Basic usage:

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

### Key Features

#### Protocol Operations

* Lending and borrowing
* Liquidity provision
* Perpetual trading
* Staking and restaking
* Yield farming
* CDP management
* Portfolio management

#### Developer Tools

* Transaction simulation
* Position monitoring
* Risk assessment

### Use Cases

Edwin enables the creation of sophisticated DeFAI agents. Here are just a few examples of what you can build:

* **Yield Optimization**: Automate staking and lending strategies across protocols
* **Liquidity Management**: Deploy and manage pool positions
* **Portfolio Management**: Handle cross-protocol positions
* **Arbitrage**: Execute cross-protocol opportunities
* **Risk Analysis**: Monitor protocol health and assess investment risks
* **Market Sentiment**: Analyze on-chain data for market trends
* **Dynamic Rebalancing**: Maintain optimal portfolio allocations based on market conditions

The possibilities are endless - as DeFAI evolves, new use cases emerge daily.

### Popular Links

* [GitHub Repository](https://github.com/edwin-finance/edwin)
* [Discord Community](https://discord.gg/2NKmbNhM)
* Telegram Community
* Twitter Page

### Contributing

Edwin is an open-source project welcoming contributions from the community:

* Bug reports
* Feature requests
* Protocol integrations
* Framework adapters
* Documentation improvements

### Next Steps

1. Follow the [quickstart.md](getting-started/quickstart.md "mention") Guide
2. Explore more [Broken link](broken-reference "mention")
3. Join our [Discord](https://discord.gg/2NKmbNhM)
4. Start Building
