# API Validation Scenarios – Crypto Buy/Sell Workflow (Simulation)

## Overview
API validation ensures that backend transaction processing, wallet balances, and order statuses remain consistent with UI behavior.

---

## Core Endpoints (Simulation)

- POST /orders
- GET /orders/{id}
- GET /wallets
- GET /transactions
- GET /prices?symbol=BTC-USD

---

## Scenario 1: Place Market Buy Order

**Request:** POST /orders  
**Payload:** BUY BTC using USD amount  

### Validate:
- Status code 200 or 201
- Order ID returned
- Executed price present
- Fee value present and correct
- Total debited = amount + fee
- Response fields not null

---

## Scenario 2: Insufficient Funds

**Request:** POST /orders  

### Validate:
- 4xx error returned
- Clear error message
- No transaction created
- Wallet balances unchanged

---

## Scenario 3: Wallet Balance After Trade

**Request:** GET /wallets  

### Validate:
- USD balance decreased correctly
- BTC balance increased correctly
- Decimal precision matches asset rules

---

## Scenario 4: Transaction History Integrity

**Request:** GET /transactions  

### Validate:
- Trade appears once (no duplicates)
- Correct timestamp ordering
- Amounts match executed trade

---

## Scenario 5: Performance & Resilience

### Validate:
- Response time within acceptable range
- Timeout errors handled consistently
- Order status reconcilable after temporary failures
