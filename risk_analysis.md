# Risk Analysis – Crypto Buy/Sell Workflow (Simulation)

## Overview
Crypto exchanges operate in high-risk financial environments where incorrect calculations, delays, or inconsistencies can directly impact user funds and trust.

This document outlines key risk areas and QA focus points.

---

## High-Risk Areas

### 1. Incorrect Fee Calculation
**Risk:** Overcharging or undercharging users  
**Impact:** Financial loss, regulatory exposure, trust damage  
**QA Focus:** Validate fee formula, rounding logic, and UI/backend consistency

---

### 2. Wallet Balance Desynchronization
**Risk:** UI balance differs from backend ledger  
**Impact:** Users make decisions based on incorrect data  
**QA Focus:** Post-trade balance validation, API/UI comparison, refresh behavior

---

### 3. Decimal Precision & Rounding Errors
**Risk:** Small rounding errors accumulate over time  
**Impact:** Ledger inaccuracies, reconciliation issues  
**QA Focus:** Asset-specific precision validation and consistent rounding rules

---

### 4. Duplicate Order Execution
**Risk:** Multiple orders created due to double submit or retries  
**Impact:** Unintended financial transactions  
**QA Focus:** Button debouncing, idempotency behavior, transaction uniqueness

---

### 5. API Timeout or Partial Failure
**Risk:** Order executes but UI shows failure (or vice versa)  
**Impact:** Inconsistent order status, user confusion  
**QA Focus:** Order reconciliation logic and consistent status messaging

---

### 6. Price Volatility During Confirmation
**Risk:** Price changes between preview and execution  
**Impact:** User disputes and trust issues  
**QA Focus:** Confirmation prompts and execution price transparency

---

## Regression Hotspots
- Wallet balance updates
- Fee display consistency
- Transaction history ordering
- Order status accuracy
- Error messaging clarity

---

## QA Mitigation Strategy
- Risk-based prioritization of financial accuracy
- Backend validation after every transaction
- Negative testing for timeouts and retries
- Clear defect documentation with reproducible steps
