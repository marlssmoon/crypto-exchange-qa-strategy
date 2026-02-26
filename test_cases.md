# Test Cases – Crypto Buy/Sell Workflow (Simulation)

## Legend
- Severity: Low / Medium / High / Critical
- Type: Smoke / Functional / Regression / Exploratory

---

### TC-01: Smoke – Market Buy Success (USD → BTC)
**Type:** Smoke  
**Preconditions:** User A has USD 500.00  
**Steps:**
1. Select BTC-USD
2. Choose Market Buy
3. Enter $100
4. Confirm transaction
**Expected Result:**
- Order confirmation displayed
- USD balance reduced by $100 + fee
- BTC balance updated correctly
- Transaction recorded in history

---

### TC-02: Smoke – Market Sell Success (BTC → USD)
**Type:** Smoke  
**Preconditions:** User A has BTC > 0  
**Steps:**
1. Select BTC-USD
2. Choose Market Sell
3. Enter sell amount
4. Confirm transaction
**Expected Result:**
- USD balance increases minus fee
- BTC balance decreases accordingly
- Transaction recorded correctly

---

### TC-03: Functional – Insufficient USD Funds
**Severity:** High  
**Preconditions:** User B has USD 0.00  
**Steps:**
1. Attempt to Buy $50 BTC
2. Confirm
**Expected Result:**
- Error message displayed
- No wallet changes
- No transaction created

---

### TC-04: Functional – Insufficient BTC Funds
**Severity:** High  
**Preconditions:** User B has 0 BTC  
**Steps:**
1. Attempt Sell BTC
2. Confirm
**Expected Result:**
- Error message displayed
- No wallet changes

---

### TC-05: Functional – Fee Calculation Accuracy
**Severity:** High  
**Steps:**
1. Buy $100 BTC with 0.10% fee
**Expected Result:**
- Fee calculated correctly
- Total debit equals $100 + fee
- UI and backend values match

---

### TC-06: Regression – Wallet Balance Sync
**Severity:** Critical  
**Steps:**
1. Complete a trade
2. Refresh page
3. Navigate to wallet
**Expected Result:**
- Balances remain accurate
- No UI/backend mismatch

---

### TC-07: Exploratory – Rapid Double Submit
**Severity:** Critical  
**Steps:**
1. Click Confirm multiple times quickly
**Expected Result:**
- Only one order executed
- No duplicate transactions

---

### TC-08: Functional – Decimal Precision Handling
**Severity:** High  
**Steps:**
1. Enter amount with many decimals
**Expected Result:**
- Proper rounding rules applied
- Backend matches UI value

---

### TC-09: Regression – Transaction History Order
**Severity:** Medium  
**Steps:**
1. Execute multiple trades
2. Open transaction history
**Expected Result:**
- Newest transaction appears first
- No missing or duplicated records

---

### TC-10: Exploratory – Network Interruption During Trade
**Severity:** Critical  
**Steps:**
1. Submit order
2. Simulate connection loss
**Expected Result:**
- Clear user messaging
- Order status reconciled correctly
