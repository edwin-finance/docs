---
icon: bullseye-arrow
---

# Quickstart

## Using Edwin Capabilities&#x20;

Edwin comes with a modular DeFAI system that can be used either stand alone or as part of an integration into an agent framework.

To use Edwin as a standalone package, follow these steps:

{% include "../.gitbook/includes/example-code-block.md" %}

## Usage within an Agent

Choose an AI Agent framework - we will use elizaOS in this example.

1. Clone the Eliza repo from [https://github.com/elizaOS/eliza](https://github.com/elizaOS/eliza).
2. Inside the `packages` directory, clone the Edwin plugin for Eliza: [https://github.com/edwin-finance/eliza-plugin-edwin](https://github.com/edwin-finance/eliza-plugin-edwin)
3. Configure your `.env`with required secrets, and configure your agent character settings under `characters`.&#x20;
4. Run the agent and use DeFAI capabilities!
