# Defiguard Backend

> Security scanning and risk analysis engine for Soroban smart contracts on the Stellar network.

## Overview

The Defiguard backend powers the contract analysis system that evaluates Soroban smart contracts deployed on the Stellar blockchain.

It performs security checks, generates risk scores, and produces security reports that can be accessed through the Defiguard frontend or stored on-chain through smart contracts.

The backend acts as the bridge between the user interface, the blockchain infrastructure, and the smart contract registry.

## Responsibilities

- Smart contract analysis
- Risk score generation
- Security report creation
- API services for frontend applications
- Interaction with Soroban smart contracts
- Data indexing and caching

## Architecture

```
Frontend Dashboard → Backend Security Engine → Soroban Smart Contracts → Stellar Blockchain
```

## Technology Stack

| Layer | Technology |
|---|---|
| Backend Framework | Node.js / NestJS |
| Database | PostgreSQL |
| Caching Layer | Redis |
| Blockchain Integration | Stellar SDK |
| Smart Contract Interaction | Soroban RPC |

## Project Structure

```
src/
├── controllers/   API endpoints
├── services/      Contract analysis and business logic
├── blockchain/    Soroban contract interactions
├── database/      Database models and repositories
└── utils/         Helper functions
```

## Prerequisites

- Node.js (v18 or higher)
- PostgreSQL
- npm or yarn

## Installation

Clone the repository:

```bash
git clone https://github.com/your-org/defiguard-backend.git
```

Navigate to the project directory:

```bash
cd defiguard-backend
```

Install dependencies:

```bash
npm install
```

Create the environment file:

```bash
cp .env.example .env
```

Then update the configuration values in `.env`.

## Running the Server

Development mode:

```bash
npm run start:dev
```

Server runs at `http://localhost:3000`.

## API Endpoints

**Scan a contract:**

```
POST /scan-contract
```

**Get risk score:**

```
GET /contracts/:address/risk
```

**Retrieve security report:**

```
GET /contracts/:address/report
```

## Security Considerations

The backend ensures accurate contract analysis by combining static security checks with blockchain data verification.

Future improvements will include automated vulnerability detection and real-time monitoring of smart contract activity.

## Ecosystem Impact

Defiguard enhances the safety of decentralized finance on Stellar by providing accessible security insights for smart contracts.

This infrastructure allows users and developers to make more informed decisions when interacting with DeFi protocols.

## Roadmap

### Phase 1

- Contract scanning API
- Risk score generation

### Phase 2

- Automated vulnerability detection
- Real-time contract monitoring

### Phase 3

- AI-powered contract security analysis
- Integration with Stellar DeFi platforms

## License

MIT License

---

**Built with ❤️ on Stellar**
