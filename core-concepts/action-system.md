---
icon: square-terminal
---

# Action System

## Overview

Actions are the fundamental building blocks of DeFAI operations in Edwin. They represent standardized operations that AI agents can execute across different protocols and chains. Each action is designed to be atomic, predictable, and composable, enabling AI agents to build complex DeFAI strategies.

## Action Types

Edwin supports a comprehensive set of DeFAI actions:

### Lending & Borrowing
- Supply assets to lending markets
- Withdraw supplied assets
- Borrow against collateral
- Repay borrowed positions

### Trading & Liquidity
- Swap tokens
- Add liquidity to pools
- Remove liquidity
- Manage LP positions

### Staking & Yield
- Stake tokens
- Unstake positions
- Claim rewards
- Reinvest yields

## Action Lifecycle

Each action follows a simple execution pattern:

```typescript
// Supply action
const supplyResult = await edwin.actions.supply.execute({
    protocol: 'aave',
    chain: 'base',
    amount: '40000',
    asset: 'usdc'
});

// Swap action with required parameters
const swapResult = await edwin.actions.swap.execute({
    protocol: 'uniswap',
    chain: 'base',
    contract: '0x...',  // Pool contract address
    amount: '1000',
    tokenIn: 'usdc',
    tokenOut: 'eth',
    slippage: 0.5,
    asset: 'usdc'
});
```

## Action Composition

Actions can be composed together to create sophisticated DeFAI strategies:

```typescript
// Multi-step DeFAI operation
async function optimizeYield() {
    // Supply collateral
    await edwin.actions.supply.execute({
        protocol: 'aave',
        chain: 'base',
        amount: '40000',
        asset: 'usdc'
    });

    // Borrow against collateral
    await edwin.actions.borrow.execute({
        protocol: 'aave',
        chain: 'base',
        amount: '5',
        asset: 'eth'
    });

    // Stake borrowed assets
    await edwin.actions.stake.execute({
        protocol: 'lido',
        chain: 'base',
        amount: '5',
        asset: 'eth'
    });
}
```

Through the action system, AI agents can create, execute, and compose DeFAI operations while maintaining predictability and safety across different protocols and chains.

