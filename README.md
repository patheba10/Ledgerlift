# LedgerLift

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
![GitHub Issues](https://img.shields.io/github/issues/monark-community/ledgerlift)

**Solution d'analyse blockchain transformant les transactions crypto en rapports financiers conformes.**

## 📋 Overview

LedgerLift permet aux utilisateurs de connecter leurs portefeuilles blockchain, récupérer leurs transactions, les classifier et générer des rapports financiers exploitables pour la comptabilité et la fiscalité.

**Cibles :** Investisseurs, DAOs, entreprises crypto, comptables.

## ✨ Key Features

- 🔐 Authentification Web3 (MetaMask, WalletConnect)
- ⛓️ Multi-chaînes (Ethereum, Polygon, BSC, Arbitrum, Optimism, Solana)
- 💵 Enrichissement prix historiques (CoinGecko)
- 🏷️ Classification (Revenus, Dépenses, Swaps, Gas, etc.)
- 📊 Rapports & Statistiques (Plus-values/Moins-values)
- 💾 Export CSV/JSON

## 🏗️ Project Structure
```
ledgerlift/
├── backend/                # Express + TypeScript + PostgreSQL
│   ├── src/
│   │   ├── controllers/    # API endpoints
│   │   ├── services/       # Business logic (auth, blockchain, price, reports)
│   │   ├── models/         # Database models (Prisma)
│   │   └── routes/         # API routes + Swagger
│   └── prisma/             # Database schema
│
├── frontend/               # Next.js + TypeScript + Tailwind
│   ├── app/                # Pages (dashboard, transactions, reports)
│   ├── components/         # UI components (shadcn-ui)
│   └── lib/                # API client, Web3 connectors
│
├── docker/
│   └── docker-compose.yml  # Full stack
│
└── docs/
    ├── SRS.pdf             # Requirements
    └── API.md              # API documentation
```

## 👥 Team

### 🔧 Binôme A : Backend & Data
- **Demba Pathe Ba** - Backend & DevOps (Express, PostgreSQL, Docker, Auth)
- **Prisciilla Vassy** - Data Blockchain (Pinax API, CoinGecko, Normalisation)

### 🎨 Binôme B : Frontend & UI
- **Hassanat Diallo** - Frontend Lead (Next.js, Tailwind, shadcn-ui, Composants)
- **Hazem Ben Chouikha** - Web3 Integrator (Wallets, API Integration, Exports)

**Superviseur :** Loucas Pelletier  
**Client :** Monark Inc.

## 🚀 Getting Started

### Prerequisites

- Node.js 20+
- Docker & Docker Compose
- PostgreSQL 15+

### Quick Start
```bash
# Clone
git clone https://github.com/monark-community/ledgerlift.git
cd ledgerlift

# Backend setup
cd backend
npm install
cp .env.example .env
# Edit .env (DATABASE_URL, API keys)
npx prisma migrate dev
npm run dev  # Runs on http://localhost:5000

# Frontend setup (new terminal)
cd frontend
npm install
cp .env.example .env.local
# Edit NEXT_PUBLIC_API_URL=http://localhost:5000
npm run dev  # Runs on http://localhost:3000
```

### Using Docker
```bash
docker-compose up -d
# Frontend: http://localhost:3000
# Backend: http://localhost:5000
```

## 🔌 API Endpoints
```
POST   /api/auth/wallet              # Connect wallet
GET    /api/wallets                  # List wallets
POST   /api/wallets/:id/sync         # Sync transactions
GET    /api/transactions             # List (paginated, filtered)
PUT    /api/transactions/:id         # Update (category, notes)
GET    /api/reports/summary          # Statistics
POST   /api/export/csv               # Generate CSV
```

**Full docs:** http://localhost:5000/api-docs

## 📜 Scripts

**Backend:**
```bash
npm run dev      # Development
npm run build    # Build
npm test         # Tests (60% coverage min)
```

**Frontend:**
```bash
npm run dev      # Development
npm run build    # Production build
```

## 🤝 Git Workflow
```bash
# Create branch
git checkout -b feature/your-name-feature

# Commit
git commit -m "feat: add wallet sync"

# Push & PR
git push origin feature/your-name-feature
```

**Commit types:** `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

## 📋 Roadmap

**Phase 1 - MVP (12 weeks)**
- Auth Web3 + Transactions (EVM/Solana)
- Classification + Reports + Export

**Phase 2 - Post-MVP (4 weeks)**
- More chains + Auto-classification + Tax reports

## 📚 Documentation

- [SRS (Requirements)](./docs/SRS.pdf)
- [Architecture](./docs/ARCHITECTURE.md)
- [API Reference](./docs/API.md)



## 📄 License

Apache License 2.0 - see [LICENSE](./LICENSE)

---
