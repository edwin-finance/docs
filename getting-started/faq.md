---
icon: question
---

# Frequently Asked Questions

## About Edwin

### What is Edwin?
Edwin is an open-source DeFAI library that serves as a bridge between AI agents and DeFi protocols. It provides a unified, secure interface for AI agents to interact with various DeFi protocols while abstracting away the complexity of blockchain operations and protocol-specific implementations.

### What is DeFAI?
DeFAI (Decentralized Finance + AI) represents the convergence of artificial intelligence and DeFi. It enables AI agents to autonomously interact with DeFi protocols, making strategic decisions and executing complex financial operations. Through Edwin, AI agents can compose sophisticated DeFAI strategies while maintaining security and predictability.

### Who is behind Edwin?
Edwin is an open-source project focused on advancing the DeFAI ecosystem. The project emphasizes community-driven development and welcomes contributions from developers, AI researchers, and DeFi enthusiasts.

### How is Edwin different from other DeFi abstraction layers?
Edwin is specifically designed for AI agents, providing an AI-native interface to DeFi protocols. While other abstraction layers focus on human developers or end-users, Edwin's architecture is built around enabling autonomous AI operations through standardized actions, protocol abstractions, and framework adapters.

## Getting Started

### How can I get started with Edwin?
Getting started with Edwin is straightforward:
1. Install the SDK: `pnpm install edwin-sdk`
2. Configure your environment with necessary keys
3. Start building your DeFAI agent

For detailed instructions, check out our [Quickstart Guide](quickstart.md).

### What protocols does Edwin support?
Edwin supports a growing list of major DeFi protocols including:
- Lending: Aave
- DEX: Meteora, Uniswap
- DEX Aggregator: Jupiter
- Data Providers: Cookie, eOracle
- And more...

### What AI frameworks can I use with Edwin?
Edwin currently provides first-class support for the Eliza and LangChain frameworks, with plans to support more AI frameworks in the future. The framework adapter system makes it easy to integrate new AI frameworks. Learn more in our [AI Framework Adapters](../core-concepts/framework-adapters.md) documentation.

### Do I need any special credentials or API keys?
You'll need:
- Private keys for the chains you want to interact with
- API keys for any specific protocols that require them

All sensitive information is handled securely through environment variables.

## Technical Overview

### What are the key components of Edwin?

Edwin's architecture consists of several key components:

**Protocol Abstraction Layer**
Creates a unified interface across different protocols. Learn more in our [Protocol Abstraction](../core-concepts/protocol-abstraction.md) documentation.

**Action System**
Provides standardized operations for AI agents to execute. See the [Action System](../core-concepts/action-system.md) documentation for details.

**AI Framework Adapters**
Enables seamless integration with AI frameworks. Check out our [AI Framework Adapters](../core-concepts/framework-adapters.md) documentation.

**Security Model**
Ensures safe and controlled DeFi operations. Read more in our [Security Model](../core-concepts/security-model.md) documentation.

### I need to integrate with a protocol you don't support. Should I use Edwin or look for another solution?
The power of Edwin extends beyond just its protocol inventory; it is built primarily as a translational
layer designed to handle everything needed for new protocols to be fully compatible with AI agents, offering
out-of-the-box transaction handling and security features. The open-source nature of Edwin provides agent builders
with the best possible headstart by enabling seamless integration of new protocols to leverage its features
without needing to start from scratch.

## Token and Community

### How do I qualify for the airdrop?
The airdrop is designed to reward meaningful contributions to the DeFAI ecosystem. For detailed eligibility criteria, check our [Tokenomics](tokenomics.md) documentation.

### How can I contribute to Edwin?

**Technical Contributions**
- Implement new protocol integrations
- Add new action types
- Improve core functionality
- Enhance documentation

**Non-Technical Contributions**
- Create educational content
- Build community resources
- Share novel DeFAI strategies
- Participate in discussions

## Future and Development

### What are the future plans for Edwin?
The team is actively working on:
- Adding more protocol integrations
- Supporting additional AI frameworks
- Enhancing the action system
- Fostering community growth

### How can protocols integrate with Edwin?
Protocols can integrate with Edwin by implementing our standardized interfaces. This makes your protocol immediately accessible to all AI agents using Edwin. Check our documentation for integration guidelines.

### How can AI frameworks integrate with Edwin?
AI frameworks can integrate through our framework adapter system. This allows AI agents built with your framework to seamlessly interact with all supported DeFi protocols. See our [AI Framework Adapters](core-concepts/framework-adapters.md) documentation for details. 