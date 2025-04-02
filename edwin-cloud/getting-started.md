# Getting Started

## Installation

### 1. Install the edwin-client SDK
```typescript
npm install @edwin-finance/edwin-client
```

### 2. Initialize the client
```typescript
import { edwinClient } from '@edwin-finance/edwin-client';

const client = new edwinClient({
    apiKey: 'your-api-key',
    wallet: yourWallet // Your wallet implementation
});
```

### 3. Register MCP for your agent
```typescript
// Register MCP for your agent
await client.registerMCP({
    agentId: 'your-agent-id',
    supportedProtocols: ['aave', 'uniswap', 'meteora']
});
```

## Basic Usage

### Configuration
* **API Key Setup**
  * Get API key from dashboard
  * Set environment variables
  * Configure client
  * Test connection

* **Wallet Integration**
  * Implement wallet interface
  * Configure signing
  * Test wallet connection
  * Handle errors

* **Environment Setup**
  * Set up development environment
  * Configure network
  * Set up monitoring
  * Test environment

### Basic Operations
* **Token Operations**
  * Supply tokens
  * Withdraw tokens
  * Transfer tokens
  * Check balances

* **Protocol Operations**
  * Lending
  * Borrowing
  * Trading
  * Staking

* **Query Operations**
  * Get balances
  * Check positions
  * View history
  * Monitor status

### Transaction Monitoring
```typescript
// Monitor MCP status
const status = await client.getMCPStatus('your-agent-id');
console.log('MCP status:', status);
```

## Best Practices

### Security
* **API Key Management**
  * Use environment variables
  * Rotate keys regularly
  * Monitor usage
  * Set up alerts

* **Wallet Security**
  * Secure key storage
  * Implement signing
  * Handle errors
  * Monitor activity

* **Request Security**
  * Validate inputs
  * Check permissions
  * Monitor usage
  * Handle errors
