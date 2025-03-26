# edwin: The DeFAI Platform
edwin is a B2C DeFAI platform accessible via a web interface, providing two key value propositions:
* Simplify DeFi operations through a chat interface.
* Run predefined DeFi strategies similar to a cloud provider.

## Settings Panel
This section allows users to configure core aspects of their edwin experience:

* [P0] Wallet management
    * [P0] User can deposit and withdraw funds accessible from all edwin agents in the context of the user.
    * [P1] Multiple wallets, each attributed to a set of agents.
    * [P1] Load credits using *$EDWIN*.
* [P1] Integrations (e.g., Twitter API, Cookie Swarm API) allow external capabilities that users can configure. Each integration can be configured multiple times under different integration names.
* [P2] RAG Integration: User need to build it itself and connect it here.
* [P2] Security
    * Usual security features of SaaS, including 2FA and other standard measures.
* [P2] Manage account
    * Set profile name.
    * Login with wallet for gated features.
    * Withdraw all funds and delete account.

## Service Agents (inspiration: OpenAI's GPT Store)
GPT store for specific DeFi protocol or interface. Chat interface that leverages a specific integration of logic implemented in the SDK, the AI wrapper is very simple for these agents.

* [P0] Each agent exposes a specific DeFi interface in a chat-like interface. Examples include:
    - Agent Meteora
    - Agent Bridge
    - Agent Uniswap
* [P0] Users can interact with any of the agents in the chat interface, similar to OpenAI's ChatGPT-store.
* [P0] Service agents are designed to execute DeFi actions on behalf of a configured wallet in the system.
* [P1] Users can view their interaction history with Service Agents.

## Autonomous Agents (inspiration: AWS)
Autnomous Agents are bots that run continously and execute DeFi operations in order to take profits. It doesn't have to be AI. If it is AI, then it can interact with the Service Agent through a text interface.

* [P1] *Runs* Page: View current and past runs of Autonomous Agents.
* [P1] *Browse* Page: Users can browse a collection of agent definitions, each implemented as code in the backend.
* [P1] *Agent Details* Page: Users can choose to start any agent. A configuration panel is provided for parameter input, similar to launching an instance on AWS.
* [P1] When starting an agents, there is a configuration panel like that AWS has when launching an instance, the user needs to fill in all parameters and variables.
* [P1] Platform Fees: 
    - The platform charges credits for executing agents.
    - The platform charges 10% of the profits an autonomous agent makes: half to the agent builder and half to
the platform.
* [P2] Each agent has it's own Terminal (See below)
* [P3] Agent builders can list their own agent.
* [P3] Allow agent builder to specify a token address for their address.

## Terminals
The terminal is the profile card of the agent, across all runs and users.

* [P2] This feature is gated with *$EDWIN*.
* [P2] Gated access also by agent's token.
* [P2] See P&L statistics of agent
* [P2] See reasoning / strategy details
* [P2] Chat interface with the agent's brain (gated by even higher amount)
* (More features, after reviewing best terminals of other agents)

-------
Token Utlities:
* Charge credits
* Gated features

Business Model:
* Fee on agents earnings.
* Fee on execution of the agent (credits like AWS)

Gated Features:
* Terminal
* Chat with agent in Terminal
* Connection to Service Agents / integrations?


Open Questions:
* The GPT Store by OpenAI did not have product market fit, why would our Service Agent interface have?
* Why previous DeFi automation platforms have not succeeded? 
* Is there an agent execution layer that we can integrate with?
* Should credits be charged in *$EDWIN* or USDC? Can it be changed later?
* Fees are to the protocol or are burned? Can it be changed later?
* How agent builder can earn from the platform?
    * 5% of profits of autonomous agent execution.
* How to keep the fee amount in the protocol's hands?
* Should we drop the concepts of Service Agents and focus only on Autonomous Agents?

Notes:
Main thesis: **Consumers will look to deploy DeFi automations**.
Subthesis: The number of ways to earn money in DeFi with automations will grow.

Q: How much money in crypto is managed by consumers and how much is by businesses?
