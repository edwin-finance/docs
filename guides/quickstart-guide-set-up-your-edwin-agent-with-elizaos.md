---
icon: play
---

# Quickstart Guide: Set Up Your edwin Agent with ElizaOS

This brief guide walks you through the setup and launch of an elizaOS agent utilizing the edwin plugin.

### Prerequisites

Before you begin, ensure you have:

* Node.js (LTS version)
* pnpm package manager installed
* Git
* Basic command line/terminal proficiency
* An EVM or Solana wallet with private key access
* API key from a supported LLM provider (e.g.,  OpenAI or Anthropic)
* For Solana users: A Helius API key

### Installation and Configuration

#### 1. Clone the Repositories

Start by cloning the necessary repositories:

```bash
git clone https://github.com/elizaOS/eliza.git
git clone -b preconfigured --single-branch https://github.com/edwin-finance/elizaos-plugin-edwin
cd eliza
git checkout v0.25.9 # The latest stable release
pnpm install --no-frozen-lockfile
```

#### 2. Install the edwin Plugin

Add the edwin plugin to your elizaOS instance:

```bash
npx elizaos plugins add @elizaos-plugins/plugin-edwin 
```

Copy the latest plugin code and update dependencies:

```bash
cp -r ../elizaos-plugin-edwin/ ./packages/plugin-edwin/
pnpm install --no-frozen-lockfile
```

#### 3. Set Up Character Profile

Place the `edwin.character.json` configuration file in the `characters` folder of your elizaOS installation.

{% file src="../.gitbook/assets/edwin.character.json" %}

**Important:** Edit the character file to specify your preferred LLM provider. For example, if using Anthropic, ensure the file contains:

```json
"modelProvider": "anthropic"
```

Match this setting to the API key you'll configure in step 5.

#### 4. Build the Application

Compile the plugin and elizaOS:

```
pnpm build
```

#### 5. Configure Wallet and API Keys

Create your environment configuration:

```
cp .env.example .env
```

In the `.env` file:

**For EVM chains:**

* Set `EVM_PRIVATE_KEY` with your wallet's private key

**For Solana:**

* Set `SOLANA_PRIVATE_KEY` with your wallet's private key
* For Meteora integration: Obtain a Helius API key and set `SOLANA_RPC_ENDPOINT` accordingly

**LLM Configuration:**

* Add your LLM provider API key (e.g., set `ANTHROPIC_API_KEY` for Anthropic)
* Make sure your character file specifies the correct model provider (e.g., `"modelProvider": "anthropic"`)

#### 6. Launch Your Agent

Start the elizaOS agent with:

```bash
pnpm start --character "characters/edwin.character.json"
```

#### 7. Verify Successful Installation

You should see the following banner in your terminal, confirming edwin is properly loaded:

```bash
┌═════════════════════════════════════┐
│            EDWIN PLUGIN             │
│                 ,_,                 │
│                (o,o)                │
│                {`"'}                │
│                -"-"-                │
├─────────────────────────────────────┤
│  Initializing Edwin Plugin...       │
│  Version: 0.0.1                     │
└═════════════════════════════════════┘
[2025-03-19 20:10:53] INFO: edwin loaded plugins: [
    "@elizaos-plugins/plugin-edwin"
]
```

#### 8. Using Your edwin-Enabled Agent

On another terminal window, launch the client interface:

```
pnpm start:client
```

Access the interface at [http://localhost:5173/](http://localhost:5173/) and begin leveraging edwin for your DeFi operations.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>



Congratulations! Your elizaOS agent is now running with the edwin plugin installed and ready to use.
