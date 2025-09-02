# Summary
Nova Indexer is an open-source DeFi indexer with native Stellar support, transforming raw on-chain events into actionable financial insights like P&L, health factors, and liquidation risks, optimized for Soroban's high-throughput architecture in payments, tokenized assets, and DeFi.

Nova integrates directly with Stellar through a chain adapter that normalizes Horizon and Soroban events, a Wasm executor that runs finance-aware modules (e.g., P&L, liquidation risk, claimable rewards), and an ingest orchestrator that enables sub-second push streams via Redis/WS. This ensures wallets, dApps, and protocols can access real-time financial insights without building custom indexers. Nova’s phased rollout begins with testnet support, then expands to mainnet deployment, advanced analytics, and community-driven module development.

# Core Architecture
Nova's design has three simple layers:

1. Chain Adapters: Normalize data from various chains (EVM, Move, Solana, Stellar, etc.).
2. Wasm Executors: Run protocol-specific logic in reusable, secure Wasm "packs" (e.g., for Aave, Uniswap, or Jupiter).
3. Ingest Orchestrator: Handles syncing blocks, routing events, and pushing updates via streams—no more slow polling.

Nova supports multiple chains out of the box: add a new chain with a lightweight adapter or a protocol with a Wasm pack. It connects to apps like Tokenpad and backend services via cloud streams, and can fall back to other indexers like DeBank or The Graph if needed.

Nova isn't just data—it's a smart engine delivering fast, accurate DeFi insights for wallets, dApps, and protocols across chains.

**Nova starts with Stellar out of the box:** add a new protocol with a Wasm pack. It connects to apps like wallets and backend services via streams, and can fall back to other indexers like The Graph if needed. Nova isn't just data—it's a smart engine delivering fast, accurate DeFi insights for wallets, dApps, and protocols, beginning with Stellar.

**What Nova Solves:** Raw indexers stop at transfers, forcing devs to code P&L and health math themselves—Nova fixes this with finance-aware Wasm modules for Stellar DEXs, AMMs, lending, and perps, so apps can query "Am I up or down?" in one call. Poll-based APIs cause 30-60s lag, missing liquidations—Nova provides sub-second push streams (Redis/WS) so wallets and bots react in under 2 seconds. Each chain needs custom tools—Nova offers unified adapters and API schema to reuse code and fund one tool. Closed vendors lock data and charge high fees—Nova's open-source core with MIT license makes it auditable, forkable, and grant-eligible.



