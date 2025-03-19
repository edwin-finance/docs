---
icon: play
---

# Quickstart Guide: Set Up Your Edwin Agent with ElizaOS

This brief guide walks you through the setup and launch of an elizaOS agent utilizing the Edwin plugin.

#### 1. Install the latest releases of elizaOS and Edwin&#x20;

Ensure you have Node.js installed.

```bash
git clone ttps://github.com/elizaOS/eliza.git
git clone -b preconfigured --single-branch https://github.com/edwin-finance/elizaos-plugin-edwin
cd eliza
git checkout v0.25.9 # The latest stable release
pnpm install --no-frozen-lockfile
```

#### 2. Add the Edwin Plugin

Install the edwin plugin:

```bash
npx elizaos plugins add @elizaos-plugins/plugin-edwin 
```

Make sure to get the latest edwin plugin code on top and get the latest packages:

```bash
cp -r ../elizaos-plugin-edwin/ ./packages/plugin-edwin/
pnpm install --no-frozen-lockfile
```

#### 3. Configure elizaOS with the edwin plugin and character profile

* Place the following character file in the characters folder:

{% file src="../.gitbook/assets/edwin.character.json" %}

#### 3. Build the plugin and eliza

```
pnpm build
```

#### 4.  Set up an EVM or Solana wallet for your agent

Copy the .env.example:

```
cp .env.example .env
```

For EVM:  Set the `EVM_PRIVATE_KEY` in your `.env` file.

For Solana:  Set the `SOLANA_PRIVATE_KEY` in your `.env`. If you are planning to use Edwin for Meteora, it is recommended that you use a Helius RPC endpoint. Get a Halius API key here (Helius link) and then set it in `SOLANA_RPC_ENDPOINT`.

Also set up an LLM API key for your agent:

* For example, for Claude, specify "modelProvider": "anthropic" in your character file, and provide an  ANTHROPIC\_API\_KEY in your `.env`file.

#### 5.  Run Your elizaOS Agent

```bash
pnpm start --character "characters/edwin.character.json"
```

#### 5. Verify Edwin is Loaded

After startup, ensure your logs mention Edwin, confirming successful loading:

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

Your elizaOS agent is now running with Edwin! Open the client and try to use it to perform DeFi operations.

```
pnpm start:client
```

Go to [http://localhost:5173/](http://localhost:5173/) and use edwin to dominate DeFi-

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>
