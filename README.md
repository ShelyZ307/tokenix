# Tokenix – Secure Digital Wallet for Blockchain Tokens

Tokenix is a FinTech & Cyber project to build a secure digital wallet for creating, storing and transferring blockchain tokens. The system uses a single smart contract written in Solidity (OpenZeppelin) to mint and manage a custom token. Users create accounts and generate key pairs locally; the backend handles authentication, transaction management and interaction with the blockchain. Communication is over HTTPS/TLS and all sensitive data is encrypted in storage. The wallet provides a minimal interface for viewing balances, transferring tokens and auditing transaction history. The project emphasises strict security, containerised deployment and test-driven development.

## Main Functional Requirements

- Create a new user account and generate a key pair for encryption and signing.
- Display the balance of tokens in the wallet, including token identifier.
- Transfer tokens between users with status updates (Pending, Confirmed, Failed) and record transactions in an audit log.
- Provide access to transaction history per user.

## Non -Functional Requirements

- Use HTTPS for all communication.
- Securely store passwords and sensitive data in a cloud database.
- Use containers (Docker) for portability and environment parity.
- Support horizontal scalability of services.
- Write unit tests (TDD) for every component.

## Technology Mapping

| Layer     | Proposed technologies                                                      |
|-----------|----------------------------------------------------------------------------|
| Frontend  | React or another modern framework, with client-side key management.        |
| Backend   | Node.js/Express or Python FastAPI for authentication, API endpoints and blockchain interaction. |
| Smart Contract | Solidity with OpenZeppelin for a single token contract.                 |
| Database  | PostgreSQL or MongoDB in the cloud.                                        |
| DevOps    | Docker, Docker Compose, CI/CD (GitHub Actions), deployment to a cloud service. |

## Security and STRIDE

The project includes a STRIDE analysis to identify threats (Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege) and defines mitigations such as strong authentication, digital signatures, encryption of data in transit and at rest, audit logging and traffic monitoring.

## Design and Testing

The system is designed using UML principles, including Use Case, Sequence, Class and ERD diagrams. Tests will be written according to TDD: test cases are defined before implementing functionality, using appropriate test frameworks (e.g. Jest/pytest) to ensure each unit meets requirements.

## Work Plan

1. Define the smart contract and deploy it in a test environment.
2. Set up the client environment that stores and manages keys.
3. Develop the backend for user authentication, transaction management and blockchain integration.
4. Integrate end-to-end security (TLS, encryption, signatures).
5. Build a basic user interface to display balances and perform transfers.
6. Write unit and integration tests for each component.
7. Create Docker configuration and CI/CD pipeline for automated deployment.
