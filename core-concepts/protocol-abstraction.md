---
icon: cloud-minus
---

# Protocol Abstraction

## The DeFi Protocol Landscape

The DeFi ecosystem is a vibrant but complex landscape of protocols, each with its own unique interfaces, parameters, and operational models. From lending platforms to decentralized exchanges and liquid staking solutions, each protocol has developed its own way of handling transactions, managing positions, and interacting with users.

This diversity, while fostering innovation, creates significant complexity. Each protocol requires specific knowledge of its interfaces, parameters, and operational nuances. For AI agents and developers, this means learning and maintaining multiple integration points, handling different error cases, and managing protocol-specific quirks.

## Universal DeFAI Language

Edwin introduces a universal language for DeFAI operations, transforming complex protocol-specific interactions into simple, standardized commands. This abstraction layer acts as a universal translator, allowing AI agents to speak one language while interacting with any supported DeFi protocol.

### Example: Supply Command

```typescript
await edwin.actions.supply.execute({
    protocol: 'aave',
    chain: 'base',
    amount: '100',
    asset: 'usdc'
});
```

In this example, the same simple command structure works seamlessly across different lending protocols, despite their underlying differences in implementation.

## Protocol Categories Made Simple

### Lending & Borrowing
Edwin standardizes core lending operations across protocols:
- Supply assets
- Borrow against collateral
- Repay loans

Whether you're interacting with established lending markets or innovative new platforms, the commands remain consistent and intuitive.

### Trading & Liquidity
For decentralized exchanges and liquidity protocols:
- Add liquidity
- Remove liquidity
- Swap tokens

One set of commands works across various DEX designs and liquidity pool structures.

### Staking & Yield
Standardized operations for yield generation:
- Stake tokens
- Claim rewards
- Track yield

For a detailed understanding of the action system, refer to the [Action System](action-system.md) documentation.
## Multichain by Design

Protocol abstraction in Edwin extends across multiple blockchain networks. The same commands work consistently across different chains, abstracting away the complexity of:
- Chain-specific transaction formats
- Different consensus mechanisms
- Varying gas models
- Network-specific parameters

### Example: Multichain Operation

```typescript
// Supply USDC on Base
await edwin.actions.supply.execute({
    protocol: 'aave',
    chain: 'base',
    amount: '100',
    asset: 'usdc'
});

// Supply USDC on Solana
await edwin.actions.supply.execute({
    protocol: 'solend',
    chain: 'solana',
    amount: '100',
    asset: 'usdc'
});
```

## Security Through Standardization

Protocol abstraction enhances security through standardization. Edwin's protocol whitelisting approach ensures that:

- Only vetted and audited protocols can be integrated
- Operations follow predefined safety boundaries
- Transactions are validated consistently
- Risk parameters are standardized across protocols

This standardization creates a secure foundation for AI agents to interact with DeFi protocols, reducing the risk of errors and ensuring predictable behavior across the entire DeFi landscape.

Learn more about our security approach in the [Security Model](security-model.md) documentation.

