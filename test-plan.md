# QA Test Plan – Crypto Buy/Sell Workflow (Simulation)

## Objective
Validate quality, reliability, and correctness of the Buy/Sell workflow across UI and backend systems, ensuring accurate balances, fees, and transaction history updates.

## Scope
### In Scope
- Buy crypto (Market)
- Sell crypto (Market)
- Fee calculation and display
- Wallet balance updates (USD + crypto)
- Transaction history updates
- Error handling and user messaging
- API/UI consistency checks

### Out of Scope
- KYC onboarding flows
- Deposits/withdrawals to external wallets
- Advanced order types (limit/stop) unless added later

## Test Types
- Smoke: basic buy/sell success paths
- Functional: validations, edge cases, negative testing
- Regression: wallet, fees, history, order status, UI/API sync
- Exploratory: behavior under interruptions, rapid changes, unexpected inputs
- API validation: response integrity, error handling, performance checks

## Test Data
- User A: USD balance = 500.00, BTC = 0.01000000
- User B: USD balance = 0.00, BTC = 0.00000000
- Fee example (simulation): 0.10%

## Environments (Simulation)
- Web UI (Chrome, Firefox)
- Mobile UI (iOS/Android)
- API endpoints (staging)

## Entry Criteria
- Feature deployed to test environment
- Test accounts available
- API endpoints reachable
- Known critical issues documented

## Exit Criteria
- All smoke tests pass
- No open critical/high defects
- Regression suite completed for impacted areas
- Defect trends summarized (severity, frequency, risk areas)

## Reporting
- Defects tracked in JIRA with: steps, expected vs actual, evidence, environment, logs (if available)
- Daily QA summary: executed cases, pass/fail rate, blockers, defect themes
