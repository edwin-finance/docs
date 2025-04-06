---
icon: play
---

# Quickstart Guide: Using the MCP Server

This is an example implementation of a Model Context Protocol (MCP) server for the edwin SDK. It allows AI agents to interact with edwin's tools through a standardized protocol.

### Prerequisites

* Node.js >= 18.0.0
* pnpm (recommended) or npm
* A local Claude instance or access to Claude API
* EVM and/or Solana wallet private keys (depending on your needs)

### Installation

1. Clone [edwin repository](https://github.com/edwin-finance/edwin) and navigate to the mcp-server directory:

```
cd examples/mcp-server
```

2. Install dependencies:

```
pnpm install
```

3. Create your environment file:

```
cp .env.example .env
```

4. Configure your `.env` file with your settings:
   * Set your wallet private keys
   * Configure the server port and name
   * Set up auto-approve settings if needed

### Configuration

The server can be configured through environment variables or programmatically. Here are the main configuration options:

* `MCP_PORT`: Port to run the server on (default: 3333)
* `MCP_SERVER_NAME`: Name of the server (default: "edwin-mcp")
* `MCP_SERVER_VERSION`: Server version (default: "0.1.0")
* `MCP_AUTO_APPROVE_ALL`: Whether to auto-approve all tool executions
* `MCP_AUTO_APPROVE_TOOLS`: Comma-separated list of tools to auto-approve
* `EVM_PRIVATE_KEY`: Your EVM wallet private key
* `SOLANA_PRIVATE_KEY`: Your Solana wallet private key
* `LOG_LEVEL`: Logging level (info, error, warn, debug)

### Running the Server

#### Development Mode

```
pnpm dev
```

This will start the server in development mode with hot reloading.

#### Production Mode

```
pnpm start
```

#### Building for Production

```
pnpm build
```

### Using with Claude

1. Start the MCP server using one of the commands above.
2.  The server will expose your edwin tools through the MCP protocol at:

    ```
    http://localhost:3333
    ```
3. Configure your Claude instance to use the MCP server:
   * Set the MCP server URL in your Claude configuration
   * Ensure your Claude instance has the necessary permissions to access the server
4. Your Claude instance can now use the edwin tools through the MCP protocol.

### Available Tools

The server exposes all tools configured in your Edwin instance. Common tools include:

* Wallet operations
* Balance checking
* Transaction signing
* Token transfers
* Contract interactions

### Security Considerations

1. Never commit your `.env` file with private keys
2. Use appropriate CORS settings in production
3. Implement rate limiting for production use
4. Keep your private keys secure and never share them
5. Use `autoApproveAll` with caution in production

### Troubleshooting

1. **Server won't start**:
   * Check if the port is already in use
   * Verify your environment variables are set correctly
   * Check the logs for specific error messages
2. **Tools not available**:
   * Ensure your edwin instance is properly configured
   * Check if the tools are properly registered
   * Verify your wallet keys are correct
3. **Connection issues**:
   * Check if the server is running
   * Verify the port is correct
   * Check network connectivity
