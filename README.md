# PLSQL Project: Installment Calculation for Contracts

## Project Overview
This PLSQL project is designed to calculate installment dates and amounts for a given contract, and handle the first installment payment. The script automatically updates a new table in the database schema with the calculated installment data.

## Project Details
This project involves the creation of three tables:
- **CONTRACTS**: This table stores information about the contract, such as the Contract_ID, Contract_STARTDATE, Contract_ENDDATE, Contract_Total_Fees, Contract_Deposit_Fees, Client_ID, Contract_Payment_Type, and Notes.
- **CLIENTS**: This table stores client information such as Client_ID, Client_Name, Mobile, Address, and NID.
- **INSTALLMENTS_PAID**: This table stores paid installment information such as Installment_ID, Contract_ID, Installment_Date, Installment_Amount, and Paid.

Two primary keys are defined using the PRIMARY KEY constraint:
- The first primary key is on the Contract_ID column of the CONTRACTS table.
- The second primary key is on the Client_ID column of the CLIENTS table.

Two foreign key constraints are used:
- The first foreign key constraint links the CONTRACTS and CLIENTS tables, where the Contract_ID column in the CONTRACTS table references the Client_ID column in the CLIENTS table.
- The second foreign key constraint is in the INSTALLMENTS_PAID table with the CONTRACTS table in the Contract_ID column.

The script uses triggers to automatically calculate the installment dates and amounts for a given contract and handle the first installment payment. The script is written in SQL and PLSQL and can be executed using TOAD.

## Tools and Technologies
- SQL
- PLSQL
- Triggers
- TOAD 

## How it Works
When a new contract is added to the CONTRACTS table, the script automatically calculates the installment dates and amounts for the contract and stores them in the INSTALLMENTS_PAID table. The first installment is also handled automatically. 

The installment calculation is based on the total contract fees, the deposit fees, and the contract payment type. The script calculates the number of installments and the installment amount, and then calculates the dates for each installment based on the contract start date and end date.

If a new installment payment is made, the script updates the INSTALLMENTS_PAID table with the paid installment information. 

## Conclusion
This PLSQL project provides an automated solution for calculating installment dates and amounts for contracts, as well as handling the first installment payment. The script uses triggers to automatically update the INSTALLMENTS_PAID table with the calculated installment data. This project can be executed using TOAD and is ideal for businesses that offer installment payment options to their clients.
