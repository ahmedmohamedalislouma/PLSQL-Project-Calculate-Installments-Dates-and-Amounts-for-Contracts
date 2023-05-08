# PLSQL Project: Calculate Installments' Dates and Amounts for Contracts

## Project Description
This PLSQL script calculates the installments' dates and amounts for a given contract and handles the first installment. It then adds all new data to a new table in the database schema.

## Project Details
The project creates three tables:
- **CONTRACTS**: This table holds information about the contract, such as Contract_ID, Contract_STARTDATE, Contract_ENDDATE, Contract_Total_Fees, Contract_Deposit_Fees, Client_ID, Contract_Payment_Type, and Notes.
- **CLIENTS**: This table holds information about clients, such as Client_ID, Client_Name, Mobile, Address, and NID.
- **INSTALLMENTS_PAID**: This table holds information about paid installments, such as Installment_ID, Contract_ID, Installment_Date, Installment_Amount, and Paid.

Two primary keys are defined using the PRIMARY KEY constraint:
- The first one is on the Contract_ID column of the CONTRACTS table.
- The second one is on the Client_ID column of the CLIENTS table.

Two foreign key constraints are used:
- The first one is between the CONTRACTS and CLIENTS tables, where the client_ID column in the CONTRACTS table references the client_ID column in the CLIENTS table.
- The second one is in the INSTALLMENTS_PAID table with the CONTRACTS table in the contract_ID column.

The script uses triggers to automatically calculate the installments' dates and amounts for a given contract and handle the first installment. The script is written in SQL and PLSQL and can be executed using TOAD.

## Tools and Technologies
- SQL
- PLSQL
- Triggers
- TOAD
