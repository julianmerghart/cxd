CxD LKA: Digital Governance Infrastructure for Sri Lanka

CxD LKA is an open-source, emergency digital governance framework designed to establish a "Shadow Constituent Assembly" or interim council support system during periods of governmental instability.

It operates on a federated, tokenless architecture utilizing donated cloud capacity, ensuring high availability and censorship resistance without the financial friction of gas fees.

🏗 System Architecture

The system is composed of three distinct layers:

The Client (Mobile PWA): A React-based Progressive Web App.

Zero-Knowledge UI: Simulates Secure Enclave signing for anonymity.

Offline-First: High-contrast, low-bandwidth design for unstable power grids.

UBI Wallet: Integrated distribution mechanism for emergency digital aid.

The Node (Consensus Engine): A lightweight C server.

Federated Byzantine Agreement (FBA): Uses Quorum Slices to reach consensus without mining.

Hardware Attestation: Verifies votes via device-bound keys (1 Device = 1 Vote) to prevent Sybil attacks.

Persistence: Append-only log storage with salted hashing for privacy.

The Ops Layer (Azure/Docker):

Automated deployment scripts for Azure Container Instances.

Geo-redundant configurations optimized for South Asia (Central India region).

🚀 Quick Start

Prerequisites

Node.js v18+

Docker & Azure CLI

GCC (for local server testing)

1. Run the Client

cd client
npm install
npm start



2. Build the Server Node

cd server
docker build -t cxd-node .
docker run -p 80:80 cxd-node



3. Deploy to Azure (Emergency Mode)

cd ops
./deploy_national_emergency.sh



🛡 Security & Privacy

No PII Storage: We do not store names or national IDs.

Salted Hashing: Device UUIDs are salted before hashing to prevent reverse-lookup by state actors.

Source Transparency: All consensus logic is verifiable in server/cxd_node.c.

🤝 Contributing

This is a humanitarian open-source project. We welcome PRs for:

Localization (Tamil/Sinhala) improvements.

Low-bandwidth optimization.

Integration with alternative identity providers.

MIT License. Free for use by any sovereign people.

📄 License
