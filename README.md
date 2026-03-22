# PuppyRaffle
Audit of a raffle-based smart contract analyzing randomness, fund handling, and fairness. Highlights vulnerabilities in winner selection, potential manipulation, and issues in payout logic.

# PuppyRaffle — Manual & Static Analysis Portfolio Project

## Overview
PuppyRaffle is a practical smart contract auditing project centered on manual review, static analysis, and common vulnerability classes found in real Solidity systems. It is well suited for demonstrating both code-reading discipline and exploit thinking.

## Why This Project Matters
This project covers several high-value audit themes in one codebase:
- Reentrancy
- Weak randomness
- Arithmetic issues
- Denial of service vectors
- ETH handling mistakes
- Informational and gas findings

## Objectives
- Perform structured scoping and reconnaissance
- Combine manual review with static analysis tools
- Identify exploit paths and severity levels
- Practice professional report writing

## Scope
Primary review areas:
- Raffle entry and payout logic
- Winner selection flow
- ETH transfers and refund paths
- Array and loop behaviors
- Admin or privileged actions

## Security Themes
- Reentrancy risks in external call flows
- Predictable or manipulable randomness
- Arithmetic and accounting edge cases
- Denial of service through unbounded patterns
- Unsafe ETH transfer assumptions

## What This Repository Shows
- Slither/manual review notes
- Finding writeups by severity
- Exploit hypotheses and reproduction steps
- Gas and code-quality observations
- Test cases for discovered issues

## Suggested Repository Structure
```text
PuppyRaffle/
├── README.md
├── findings/
│   ├── H-01-reentrancy.md
│   ├── M-01-weak-rng.md
│   └── L-01-eth-handling.md
├── notes/
│   ├── slither-notes.md
│   └── manual-review.md
├── poc/
│   ├── reentrancy.t.sol
│   └── dos-scenario.t.sol
└── report/
    └── audit-report.md
```

## Key Learning Outcomes
- Static analysis speeds up early reconnaissance
- Randomness is a recurring attack surface in Solidity
- ETH transfers often create hidden failure modes
- Severity depends on exploitability, not just bug presence

## Run Locally
```bash
forge install
forge build
forge test
slither .
```

## Portfolio Value
This project demonstrates practical auditing workflow: scoping, tooling, exploit identification, and polished writeups.

## Disclaimer
This repository is for educational, research, and portfolio purposes only.
