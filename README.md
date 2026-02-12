# How to Use This Template

This template helps you quickly start a **Monark project** with the **standard monorepo structure**, pre-configured licenses, policies, and workflows. It includes:

- Standardized **monorepo structure** for Monark projects.
- Predefined **issue templates** and **labels** for consistent project management.
- Guidance to get started with **Monark workflows**.

> **Tip:** Once you’ve completed these setup steps, you can delete this section from your repository.

---

## Setup Steps

1. **Replace placeholders** in your project files:  
   - `LedgerLift` → Your project name  
   - `Backend system for blockchain accounting data extraction and processing`  → Short description of the project  
   -  `accounting-blockchain-data-extraction` → GitHub repository name  
   - `2026` → Project start year  
   - `2026` → Current year  

2. **Sync repository labels with the template repository**  
   1. Make sure your **workflow permissions** are set to **Read & Write**:  
      [GitHub Actions workflow permissions](https://github.com/marketplace/actions/github-label-sync-action#403-resource-not-accessible-by-integration)  
   2. Go to the **Actions** tab in your repository and run the **`Apply Template Labels`** workflow.  
   3. Confirm that the repository now contains the **standard Monark labels** (for example, check that `P0 🟣` exists).


---

# LedgerLift

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
![GitHub Issues](https://img.shields.io/github/issues/monark-community/{{PROJECT_NAME}})
![GitHub Issues](https://img.shields.io/github/issues-pr/monark-community/{{PROJECT_NAME}})
![GitHub Stars](https://img.shields.io/github/stars/monark-community/{{PROJECT_NAME}})
![GitHub Forks](https://img.shields.io/github/forks/monark-community/{{PROJECT_NAME}})

LedgerLift is a backend system designed to extract, process, and manage blockchain accounting data within a modular monorepo architecture.

## Overview

LedgerLift provides a structured architecture for managing blockchain-derived financial data.  
The system is built around a scalable backend API using TypeScript and Node.js, and is designed to support:

- Data extraction from blockchain sources
- Processing and normalization of accounting data
- Secure API exposure
- Future smart contract integration
- Frontend dashboard integration

The backend is currently running locally on port 5000.


## Key Features

- 🚀 Modular monorepo architecture  
- ✅ TypeScript-based Express backend  
- 📊 Structured separation of controllers, services, models and routes  
- 🔐 Ready for PostgreSQL + Prisma integration  
- 🐳 Infrastructure-ready with Docker support  

## Project Structure

```
accounting-blockchain-data-extraction/
├── packages/
│ ├── shared/ # Shared types and utilities
│ ├── smart-contracts/ # Solidity contracts + ZK circuits
│ │ ├── contracts/
│ │ ├── circuits/
│ │ └── test/
│ └── subgraph/ # The Graph indexing
├── services/
│ ├── api/ # Backend API (Node.js + PostgreSQL)
│ │ ├── src/controllers/
│ │ ├── src/middlewares/
│ │ ├── src/models/
│ │ ├── src/routes/
│ │ └── src/services/
│ └── web/ # Frontend (Next.js + React - upcoming)
│ ├── app/
│ ├── components/
│ └── services/
└── infra/
└── docker-compose.yaml
```


---

## Getting Started

### 1️⃣ Navigate to API directory


### 2️⃣ Install dependencies


Open in browser:

http://localhost:5000

## Available Scripts


---

## Available Scripts

Inside `services/api`:

- `npm run dev` → Start development server with ts-node-dev  
- `npm run build` → Compile TypeScript  
- `npm start` → Run compiled production version  

---

## Deployment

Planned deployment strategy:

- Dockerized PostgreSQL database  
- Node.js backend container  
- Environment variable management  
- Cloud-ready architecture  

---

## Documentation

Documentation will include:

- API specification (OpenAPI)
- Database schema design
- Smart contract integration flow
- Security model

---

## Contribution

See [CONTRIBUTING.md](./CONTRIBUTING.md) to learn about contributions guidelines.

---

## Code of Conduct

See [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) to learn about the code of conduct.

---

## License

See the [LICENSE](./LICENSE) file to learn more about this project's licensing.


## Deployment

TODO

## Documentation

TODO

## Contribution

See [CONTRIBUTION.md](./CONTRIBUTION.md) to learn about contributions guidelines.

## Code of Conduct

See [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) to learn about the code of conduct.

## License

See the [LICENSE](./LICENSE) file to learn more about this project's licensing.
