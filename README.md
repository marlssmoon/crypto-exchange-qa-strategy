# Crypto Exchange QA Strategy (Simulation)

This repository demonstrates how I would approach QA for a regulated U.S. crypto platform’s core **Buy/Sell** transaction workflow.

## What’s Included
- **Risk-based QA Test Plan** (scope, test types, entry/exit criteria)
- **Structured Test Cases** (smoke, functional, regression, exploratory)
- **Risk Analysis** focused on financial accuracy and system consistency
- **API Validation Scenarios** aligned to fintech expectations (Postman-ready format)

## Why This Matters (Fintech Context)
Crypto exchanges operate in a high-stakes environment where defects can impact:
- user balances and transaction accuracy
- trust and customer retention
- compliance expectations in regulated systems

## Files
- `test-plan.md` – QA scope, approach, environments, criteria
- `test-cases.md` – structured test cases with steps and expected results
- `risk-analysis.md` – high-risk areas and regression hotspots
- `api-tests.md` – API validation scenarios and expected behaviors

## Assumptions (Simulation)
- Users can trade BTC using USD balance
- Fees apply to every transaction
- Orders update wallet balances and transaction history
- UI and API responses must remain consistent
