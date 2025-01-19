---
icon: 🦉
---

# 🦉 How Edwin Works

Edwin is a TypeScript library that serves as the bridge between AI agents and DeFi protocols. It provides a unified, secure interface for AI agents to interact with various DeFi protocols while abstracting away the complexity of blockchain operations and protocol-specific implementations.

## System Architecture

```mermaid
graph TB
    %% Styling
    classDef default fill:#f9f9f9,stroke:#333,stroke-width:2px
    classDef highlight fill:#e1f5fe,stroke:#01579b,stroke-width:2px
    classDef core fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px
    classDef security fill:#ffebee,stroke:#c62828,stroke-width:2px

    subgraph "AI Layer"
        A[AI Agent]
        P[Edwin Plugin]
        A --> P
    end
    
    subgraph "Edwin"
        B[Framework Adapter]
        C[Protocol Abstraction Layer]
        D[Protocol Type Interfaces]
        E[Provider System]
        
        P --> B
        B --> C
        C --> D
        D --> E
        
        subgraph "Security Layer"
            F[Transaction Validation]
            G[Protocol Whitelist]
            H[Security Checks]
        end
    end
    
    subgraph "Protocol Layer"
        I[Protocol SDKs]
        J[DeFi Protocols]
        
        E --> I
        I --> J
    end
    
    %% Security connections
    C -.-> F
    F -.-> E
    G -.-> E
    H -.-> E

    %% Apply styles
    class A,P highlight
    class B,C,D,E core
    class F,G,H security
```

## Core Components

### Protocol Abstraction Layer
The heart of Edwin is its Protocol Abstraction Layer, which provides a standardized interface for interacting with different types of DeFi protocols:

- **Lending Protocols**: Standardized interfaces for lending and borrowing operations
- **DEX Protocols**: Unified interfaces for liquidity provision and trading
- **Future Protocol Types**: Extensible system for adding new protocol categories

### Provider System
Edwin implements a sophisticated provider system that:
- Manages different protocol SDK requirements
- Handles blockchain infrastructure differences
- Provides seamless transitions between underlying implementations
- Ensures consistent interaction patterns regardless of the protocol

### Security Layer
Edwin incorporates multiple security measures to ensure safe DeFi operations:

1. **Transaction Security**
   - Transaction validation and signing
   - Amount and gas limits
   - Slippage protection
   - Failure recovery

2. **Protocol Security**
   - Whitelist verification
   - Protocol health checks
   - Operation boundaries

## Data Flow

### 1. Command Initiation
- AI agent generates a DeFi operation command
- Framework adapter normalizes the command for Edwin

### 2. Protocol Abstraction
- Command is mapped to standardized protocol interface
- Protocol type is identified (Lending, DEX, etc.)
- Provider system selects appropriate implementation

### 3. Security Checks
- Transaction validation
- Protocol whitelist verification
- Security boundaries check

### 4. Protocol Execution
- Provider executes operation through protocol SDK
- Transaction is signed and broadcast
- Result is monitored and returned

## Integration Points

### For AI Frameworks
Edwin provides a clean adapter interface that:
- Accepts standardized commands
- Handles response formatting
- Manages state updates
- Provides operation feedback

### For DeFi Protocols
Protocols can integrate with Edwin through:
- Implementation of protocol type interfaces
- Provider system adaptation
- SDK integration

## Technical Implementation

Edwin is built with TypeScript, offering:
- Modern development experience
- Easy integration with existing TypeScript/JavaScript projects
- Comprehensive type definitions for all interfaces


