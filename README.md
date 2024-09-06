# Cash-Flow-Minimizer-System
# Cash Flow Minimizer System

## Project Overview
The **Cash Flow Minimizer System** aims to optimize interbank transactions by minimizing the number of financial exchanges required among multiple banks. This system handles multiple banks, each with different payment modes, and a world bank that serves as an intermediary for banks with no common payment modes. The goal is to reduce the number of intermediary transactions and calculate a minimized cash flow that satisfies all debts and credits among the participating banks.

## Features
- Minimizes the number of transactions between banks with different payment modes.
- Utilizes a world bank as an intermediary when banks have no common payment modes.
- Determines the minimum cash flow required between banks using advanced algorithms.
- Supports multiple payment modes and ensures correct transaction matching based on these modes.
- Provides a detailed transaction log that lists all the minimized transactions required to settle debts.

## Workflow
1. **Input the participating banks and their respective payment modes.**
    - For each bank, the user must provide the bank name and the number of payment modes it supports. 
    - The first bank is always considered as the World Bank, which has all available payment modes.

2. **Input the number of transactions.**
    - The user must specify the total number of transactions between the banks.

3. **Provide transaction details.**
    - For each transaction, the user enters the debtor bank, creditor bank, and the transaction amount.
  
4. **Cash Flow Minimization Algorithm.**
    - The system calculates the net amount each bank owes or is owed, and it optimizes the number of transactions.
    - If two banks have no common payment mode, the system routes transactions through the World Bank.
    - It prints the minimized transactions, showing the reduced number of exchanges required to settle debts.

## How It Works
The program uses a greedy algorithm to minimize cash flow. Here’s the step-by-step process:
- Calculate the net balance (netAmount) for each bank based on incoming and outgoing transactions.
- For each bank with a negative balance (debtor), find a creditor with a common payment mode, or use the World Bank as an intermediary.
- Perform the minimum number of transactions required to settle debts using the most appropriate payment mode.
