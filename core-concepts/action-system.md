---
icon: square-terminal
---

# Action System

## Overview

Tools are the fundamental building blocks of DeFAI operations in edwin. They represent standardized operations that AI agents can execute across different protocols and chains. Each tool is designed to be atomic, predictable, and composable, enabling AI agents to build complex DeFAI strategies.

## Tool Types

edwin supports a comprehensive set of DeFAI tools through various plugins:

### Lending & Borrowing (Aave)
- `supply`: Supply assets to Aave protocol
- `withdraw`: Withdraw supplied assets from Aave

### Trading & Liquidity (Uniswap)
- `swap`: Swap tokens on Uniswap
- `addLiquidity`: Add liquidity to Uniswap pools
- `removeLiquidity`: Remove liquidity from Uniswap pools

### Staking & Yield (Lido)
- `stake`: Stake ETH on Lido
- `unstake`: Unstake stETH from Lido

## Tool Lifecycle

Each tool follows a simple execution pattern:

```typescript
// Supply action
const supplyResult = await edwin.plugins.aave?.supply.execute({
    chain: 'base',
    amount: 40000,
    asset: 'usdc'
});

// Swap action with required parameters
const swapResult = await edwin.plugins.uniswap?.swap.execute({
    chain: 'base',
    amount: 1000,
    tokenIn: 'usdc',
    tokenOut: 'eth',
    slippage: 0.5
});
```

## Tool Composition

Tools can be composed together to create sophisticated DeFAI strategies:

```typescript
// Multi-step DeFAI operation
async function optimizeYield() {
    // Supply collateral
    await edwin.plugins.aave?.supply.execute({
        chain: 'base',
        amount: 40000,
        asset: 'usdc'
    });

    // Borrow against collateral
    await edwin.plugins.aave?.borrow.execute({
        chain: 'base',
        amount: 5,
        asset: 'eth'
    });

    // Stake borrowed assets
    await edwin.plugins.lido?.stake.execute({
        chain: 'base',
        amount: 5,
        asset: 'eth'
    });
}
```

Through the tool system, AI agents can create, execute, and compose DeFAI operations while maintaining predictability and safety across different protocols and chains.

