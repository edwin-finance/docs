---
icon: plug
---

# AI Framework Adapters

## Framework Integration

Edwin's framework adapters provide a seamless connection between AI frameworks and DeFAI operations. Through these adapters, AI agents become autonomous actors in DeFi protocols, using their native communication patterns while Edwin handles the complexity of protocol interactions behind the scenes.

The adapter interface is designed to be lightweight and flexible, allowing AI frameworks to integrate with minimal configuration. Currently, Edwin provides first-class support for the Eliza and LangChain frameworks, enabling AI agents to autonomously execute DeFAI operations through natural conversations.

## Working with Adapters

Setting up an adapter requires minimal configuration. Here's how a typical AI agent integration flows:

```typescript
import { Edwin, EdwinConfig } from "edwin-sdk";


export async function getEdwinClient(): Promise<Edwin> {
    const edwinConfig: EdwinConfig = {
        evmPrivateKey: process.env.EVM_PRIVATE_KEY as `0x${string}`,
        solanaPrivateKey: process.env.SOLANA_PRIVATE_KEY as `0x${string}`,
        actions: ["supply", "withdraw", "stake"],
    };
    const edwin = new Edwin(edwinConfig);
    return edwin;
}

export const edwinProvider: Provider = {
    async get(runtime: IAgentRuntime): Promise<string | null> {
        try {
            const edwin = await getEdwinClient();
            const address = edwin.provider.wallets['evm'].getAddress();
            return `Edwin Wallet Address: ${address}`;
        } catch (error) {
            console.error("Error in Edwin provider:", error);
            return null;
        }
    },
};
```

Common AI agent patterns include:

* Autonomous decision execution
* Conversation-driven operations
* Multi-step strategic actions
* Position monitoring and management

Each adapter maintains consistent behavior across different protocols and chains, while providing framework-specific optimizations for better AI agent performance and operational efficiency.

## Error Handling and Feedback

Framework adapters provide structured responses that enable AI agents to make intelligent decisions. Each operation returns:

* Operation status (success/failure)
* Detailed result data
* Context for next strategic actions
* Relevant warnings or suggestions

When errors occur, adapters format the responses in a way that empowers AI agents to:

* Implement retry strategies
* Explore alternative approaches
* Manage risk exposure
* Communicate effectively with users

The adapter layer ensures that complex DeFAI operations are translated into clear, actionable feedback that AI agents can process and respond to autonomously.
